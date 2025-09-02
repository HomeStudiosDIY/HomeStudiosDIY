# Coming Soon!!

<a id="readme_top"></a>
## Frigate
Frigate is a free, open-source NVR (Network Video Recorder) system designed specifically for real-time AI-powered object detection. It’s commonly used in home automation setups, especially when privacy, performance, and local processing are a priority.  
https://frigate.video/



<summary><u>Table of Contents</u></summary>

+ <a href="#Installation">Installation</a>
	



<a href="https://github.com/HomeStudiosDIY/HomeStudiosDIY/blob/main/README.md">Back to Home Page</a>



Installation





Google Coral USB Edge TPU ML Accelerator coprocessor for Raspberry Pi and Other Embedded Single Board Computers


Google Coral - Edge TPU Accelerator - Mini PCIe - Frigate - AI - MobileNet V2


Config





bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"


Privileged


 To update Frigate, create a new container and transfer your configuration.


	mkdir /data/
	mkdir /data/config/
	mkdir /data/cctv/






```
chown 100109:100117 /mnt/pve/disk4tb/frigate/
```





pct set 104 -mp0 /mnt/pve/disk4tb/frigate,mp=/data/cctv/




from Proxmox Shell

USB Coral

nano /etc/pve/lxc/104.conf

	lxc.mount.entry: /dev/bus/usb/002/ dev/bus/usb/002/ none bind,optional,create=dir 0,0






PCIe Coral

wget -qO - https://packages.cloud.google.com/apt/doc/apt-key.gpg | gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/google.gpg --import -
rm /etc/apt/trusted.gpg.d/google.gpg~
chmod 644 /etc/apt/trusted.gpg.d/google.gpg
echo "deb https://packages.cloud.google.com/apt coral-edgetpu-stable main" | tee /etc/apt/sources.list.d/coral-edgetpu.list
apt-get update
apt-get install pve-headers libedgetpu1-std dkms devscripts dh-make dh-dkms git -y
git clone https://github.com/google/gasket-driver.git
cd gasket-driver
sed -i -e 's/no_llseek/noop_llseek/g' src/gasket_core.c
sed -i -e 's/MODULE_IMPORT_NS(DMA_BUF)/MODULE_IMPORT_NS("DMA_BUF")/g' src/gasket_page_table.c
debuild -us -uc -tc -b
cd ..
dpkg -i gasket-dkms_1.0-18_all.deb

Credit goes to Justin over at https://rovingclimber.com/2025/08/08/coral-tpu-driver-install-for-proxmox-9-0-debian-13/
If it returns an error at the last command, then download the image from here:
wget https://github.com/feranick/gasket-driver/releases/download/1.0-18.4/gasket-dkms_1.0-18.4_all.deb
And install it:
dpkg -i gasket-dkms_1.0-18.4_all.deb




lspci -nn | grep 089a

ls -la /dev/apex*




ls -l /dev/dri

ls -la /dev/apex*


lxc.cgroup2.devices.allow: c 120:0 rwm #coral 1
lxc.cgroup2.devices.allow: c 226:0 rwm #igpu
lxc.cgroup2.devices.allow: c 226:128 rwm #igpu
lxc.mount.entry: /dev/apex_0 dev/apex_0 none bind,optional,create=file
lxc.mount.entry: /dev/dri/renderD128 dev/dri/renderD128 none bind,optional,create=file 0,0 # iGPU (u=root g=render)















<p align="right"><a href="#readme_top">back to top</a></p>