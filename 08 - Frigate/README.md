# Frigate-Config-File



## FRIGATE:
<a id="about-the-project"></a>


Frigate is a free, open-source NVR (Network Video Recorder) system designed specifically for real-time AI-powered object detection. It’s commonly used in home automation setups, especially when privacy, performance, and local processing are a priority.


bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"


Privileged


 To update Frigate, create a new container and transfer your configuration.


	mkdir /data/
	mkdir /data/config/
	mkdir /data/cctv/


pct set 104 -mp0 /mnt/pve/disk4tb/frigate,mp=/data/cctv/




nano /etc/pve/lxc/104.conf

	lxc.mount.entry: /dev/bus/usb/002/ dev/bus/usb/002/ none bind,optional,create=dir 0,0






<p align="right">(<a href="#readme_top">back to top</a>)</p>