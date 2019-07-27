
---
title: "Install Information"
date: 2019-07-27T13:35:33-04:00
---
# Plymouth State Creation Technology & Hacking Club

**Welcome!**

The 'psu-hacking' disk image extends the Ubuntu LTS (18.04.2) operating system with common dependencies/software for the discerning college student.

- Live, Persistent file storage
- Fast: Ubuntu LTS + mkusb (casper-rw) = efficient
- Use (almost) any hardware- take your desktop OS with you
- Completely self sufficient: does not interact with your existing OS or other hard disks!

The current image is compiled through Cubic and burned as a persistent live OS with mkusb, using Ubuntu Desktop LTS.

# Features & Software:

- Atom editor with Chapel language support
- R language + RStudio editor / IDE
- Google Chrome
- Libre Office suite

# Make Your Own:

Thus far, the recommended way to get a persistent/live image installed is with two USB sticks:  
One completely live (not persistent) Ubuntu drive, from which you can download and run the mkusb utility on the second USB stick.

**Personal OS:**

- Download the official Ubuntu image here https://ubuntu.com/download/desktop
- Download Etcher from here https://www.balena.io/etcher/
- Use Etcher to burn Ubuntu to USB stick #1

**USB stick #1:**

- Boot from the USB stick:
	- Mac hardware- hold the alt/option key when the machine turns on
	- Other hardware- hold the boot loader key (usually F12, or F2 / F10)  when the machine turns on
- Follow the Ubuntu prompts (please avoid the host hardware’s disk, do not install anything anywhere yet)

Open a terminal and copy these commands:
```
# get the psu-hacking image for the second, persistent USB stick:
wget ||PUT HUGO URL HERE||
# get mkusb
sudo add-apt-repository universe  
sudo add-apt-repository ppa:mkusb/ppa
sudo apt-get update
sudo apt-get install mkusb mkusb-nox usb-pack-efi
```
- insert USB stick #2
- Open mkusb:
	- Follow prompts, psu-hacking iso should be in directory “home”
	- Select NO for “Quick Option” on host’s disk
	- Finish the prompts, quit, shutdown

**USB stick #2:**
- Remove drive #1
- Boot from USB stick #2:
	- Mac hardware- hold the alt/option key when the machine turns on
	- Other hardware- hold the boot loader key (usually F12, or F2 / F10)  when the machine
- Congratulate yourself, you are done!

# Building the image:
**On Ubuntu LTS**

```
# get Cubic
sudo apt-add-repository ppa:cubic-wizard/release
sudo apt update
sudo apt install cubic
```
(See /cubic_psuhacking.sh for current depends)
```
# as chroot in Cubic:
yes | sudo bash ./cubic_psuhacking.sh
```
```
# get mkusb
sudo add-apt-repository universe  
sudo add-apt-repository ppa:mkusb/ppa
sudo apt-get update
sudo apt-get install mkusb mkusb-nox usb-pack-efi
```
**Note: mkusb utility is only available for Debian/Ubuntu**


**About persistent live Ubuntu:**

When burned into a usb stick, this OS is completely self-sufficient and compatible with most (x86-64) computers- the environment, file system, preferences, etc are saved regardless of hardware.   

*Links:*
https://launchpad.net/cubic

https://help.ubuntu.com/community/mkusb
