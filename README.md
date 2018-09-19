# Tools

## OpenCV Development Environment

1. Create a virtual machine with Ubuntu Server 18.04 LTS on VirtualBox.
2. Configure the virtual machine to share a folder `Development` between the Host and Guest.
3. Install VirtualBox Guest Additions on the virtual machine with the following commands (after insert the VBoxAdditions.iso on the virtual machine):
```
mount /dev/cdrom /mnt
bash /mnt/VBoxLinuxAdditions.run

```
4. Give access to the shared folder on the guest machine located at `/media/sf_Development` to the regular user using the following command:
```
adduser <username> vboxsf
```
5. Execute the following commands to install OpenCV and dependencies:
```
apt install -y xorg
apt install -y --no-install-recommends lightdm-gtk-greeter
apt install -y --no-install-recommends lightdm
apt install -y --no-install-recommends openbox
apt install -y python3 python3-pip python3-opencv python3-numpy
apt autoremove -y
```

