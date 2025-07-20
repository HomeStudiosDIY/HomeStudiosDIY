# Work in Progress

<a id="readme_top"></a>
## Proxmox  
Proxmox delivers powerful, enterprise-grade solutions with full access to all functionality for everyone - highly reliable and secure.
The software-defined and open platforms are easy to deploy, manage and budget for.  
https://www.proxmox.com/en/

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#Installation">Installation</a>

+ <a href="#NVIDIA_Drivers">NVIDIA Drivers</a>


+ <a href="#NFS_to_NAS">Connect to your NAS with NFS</a>

	
</details>  

<a href="https://github.com/HomeStudiosDIY/HomeStudiosDIY/blob/main/README.md">Back to Home Page</a>



Here with some config settings to help you get you ProxMox Server setup and working!!  

I run all my application on a LXC inside Docker but you can run the LXC application directly this was just my preference for consistency as not all application I use can run directly on a LXC. All my LXC config and Docker Compose files will also be sheared.

https://community-scripts.github.io/ProxmoxVE/





<a id="Installation"></a>
## Installation



https://rufus.ie/en/




Proxmox installer
nomodeset


<p align="right"><a href="#readme_top">back to top</a></p>



<a id="NFS_to_NAS"></a>
## Connect to your NAS with NFS		

To connect to a NAS device with NFS you will have to setup some paths/directory’s this is how I have done mine but you can use your own location.   

If you need sub folders you will need to make the directory tree.
	
```
mkdir /mnt/data
```
```
mkdir /mnt/data/stream
```
```
mkdir /mnt/data/usb
```
```
mkdir /mnt/data/photos
```

mkdir /mnt/pve/disk4tb/frigate



mkdir /mnt/pve/disk4tb/downloads


The following will be needed to auto connect to you NFS shears.

``` 
nano /etc/fstab
```

10.0.0.1:/volume1/Stream/ /mnt/data/stream nfs defaults 0 0
10.0.0.1:/volumeUSB1/usbshare /mnt/data/usb nfs defaults 0 0
10.0.0.1:/volume1/Photos-Link /mnt/data/photos nfs defaults 0 0
10.0.0.1:/volume1/Downloads /mnt/data/downloads nfs defaults 0 0


Once you have saved your config you need to run the following.



Reload systemd:
```
systemctl daemon-reload  
```
Mount shares:
```
mount -a
```



chown 100109:100117 /mnt/pve/disk4tb/frigate/



<p align="right"><a href="#readme_top">back to top</a></p>

<a id="NVIDIA_Drivers"></a>
# NVIDIA

depending on your needs 





<a id="nvidia_drivers_proxmox"></a> 
## Install NVIDIA Drivers on ProxMox  


You will need to get the latest NVIDIA drivers from the following site

Setup Guide
```
apt update && apt upgrade -y && apt install pve-headers build-essential software-properties-common make nvtop htop -y
```
```
update-initramfs -u
```


system is now ready to get the drivers

https://www.nvidia.com/en-gb/drivers/




<img width="1544" height="531" alt="NVIDIA_get_location" src="https://github.com/user-attachments/assets/3e99584d-27c6-4294-9e59-bf277f6af1aa" />


https://uk.download.nvidia.com/XFree86/Linux-x86_64/570.172.08/NVIDIA-Linux-x86_64-570.172.08.run



wget https://uk.download.nvidia.com/XFree86/Linux-x86_64/550.142/NVIDIA-Linux-x86_64-550.142.run


Make sure you use the same file name

```
chmod +x NVIDIA-Linux-x86_64-550.144.03.run
```

```
./NVIDIA-Linux-x86_64-550.144.03.run --dkms
```



<p align="right"><a href="#readme_top">back to top</a></p>

<a id="install-nvidia-drivers-on-proxmox"></a>
## Installing NVIDIA Drivers for LXC Setup for Nvida: 

I have the following LXC setup to use my NVIDA card (Jellyfin, Plex, Ollama......)


pct push LXC_Number NVIDIA-Linux-x86_64-550.144.03.run /root/NVIDIA-Linux-x86_64-550.144.03.run


```
chmod +x NVIDIA-Linux-x86_64-550.144.03.run
```
```
./NVIDIA-Linux-x86_64-550.144.03.run --no-kernel-modules
```

```
apt install gpg curl
```


```
curl -fsSL https://nvidia.github.io/libnvidia-container/gpgkey | gpg --dearmor -o /usr/share/keyrings/nvidia-container-toolkit-keyring.gpg && curl -s -L https://nvidia.github.io/libnvidia-container/stable/deb/nvidia-container-toolkit.list | sed 's#deb https://#deb [signed-by=/usr/share/keyrings/nvidia-container-toolkit-keyring.gpg] https://#g' | tee /etc/apt/sources.list.d/nvidia-container-toolkit.list
```

```
apt update  
```
```
apt install nvidia-container-toolkit  
```

```
nvidia-smi  
```


only if you run Docker  
nvidia-ctk runtime configure --runtime=docker



Now we need to edit a file
```
nano /etc/nvidia-container-runtime/config.toml  
```


#no-cgroups = false  
to  
no-cgroups = true  


now we need to find the card details so we can map this to the LXC

```
ls -al /dev/nvidia*
```


<img width="866" height="330" alt="NVIDIA_card_details" src="https://github.com/user-attachments/assets/c6d7a02a-f831-4d3c-a65a-bdd8fb697127" />



now we need to update the config file for the LXC 



lxc.cgroup2.devices.allow: c 195:* rwm

nano /etc/pve/lxc/105.conf




	lxc.cgroup2.devices.allow: c 195:* rwm
	lxc.cgroup2.devices.allow: c 234:* rwm
	lxc.cgroup2.devices.allow: c 237:* rwm
	lxc.mount.entry: /dev/nvidia0 dev/nvidia0 none bind,optional,create=file
	lxc.mount.entry: /dev/nvidiactl dev/nvidiactl none bind,optional,create=file
	lxc.mount.entry: /dev/nvidia-modeset dev/nvidia-modeset none bind,optional,create=file
	lxc.mount.entry: /dev/nvidia-uvm dev/nvidia-uvm none bind,optional,create=file
	lxc.mount.entry: /dev/nvidia-uvm-tools dev/nvidia-uvm-tools none bind,optional,create=file
	lxc.mount.entry: /dev/nvidia-caps/nvidia-cap1 dev/nvidia-caps/nvidia-cap1 none bind,optional,create=file
	lxc.mount.entry: /dev/nvidia-caps/nvidia-cap2 dev/nvidia-caps/nvidia-cap2 none bind,optional,create=file



<p align="right"><a href="#readme_top">back to top</a></p>



