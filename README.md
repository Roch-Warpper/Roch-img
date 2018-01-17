# Roch Img
Requires Ubuntu Customization Kit 2.4.7-0ubuntu1 on Ubuntu14.04.5

## Preparation
At first should install UCK:
```
sudo apt-get install uck
```

For now should notes path of this repo, in ```build``` file:
 * UBUNTU_ISO: Path of ubuntu iso, should be input ```~/tools/ubuntu-14.04.5-desktop-amd64.iso```
 * ISO_DIR: Output with finial iso by custom, default is ```~/tmp```


## Building the ISO
--------------------------------
sudo ./build
  or
sudo uck-remaster ~/Downloads/ubuntu-14.04-desktop-amd64.iso ~/scripts_iso/roch-iso

Finially you should be find custom iso named ```livecd.iso``` in ```~/tmp/remaster-new-files/livecd.iso```

## Config Files
--------------------------------
apt_packages	List of packages to install via apt
apt_deinstall	Packages to remove from the default Ubuntu ISO
deb_packages	Packages that are not in a public repo [for testing]
pip_packages	Python packages installed via pip
inst_packages	Packages only needed for installer
patch_list	ISO patches [if all else fails]


## Notes and Known Bugs
--------------------------------
UEFI sucks and SecureBoot is designed to allow companies to control
what is installed on your computer. Demand hardware without it.
Newer machines may require UEFI, so you may or may not need to boot the
system in UEFI mode. 32-bit machines do not work with UEFI.
https://help.ubuntu.com/community/UEFI

Installing with wireless enabled seems to work slightly better.
Otherwise you may need to run the following when the system is online.
  sudo apt-get update
  sudo agt-get dist-upgrade

If wireless access points do not show up, try disabling and reenabling
the wireless network connection.

## Sponsors
--------
Development of this software for ROS Indigo has been partially sponsored by SawYer Robotics Co.,Ltd
http://www.soyrobotics.com/
