# Bash Graphical User Theme Changer (bgutc)

It is a bash script that allows tiling window manager users to create various presets for their program configurations and to switch between them quicly.

## Composition

bgutc comes with 4 files

- an Open Source bash script (/user/bin/bgutc)
- an configuration file (/home/user/.config/bgutc.conf)
- a desktop entry (/home/user/.local/share/applications/bgutc.desktop)
- an installer (update) 

### More details

#### bgutc.conf

This is the file your suppose to configure as you wish. See the Configuration section to know how to configure it.

#### bgutc.desktop

This file is necessary for app launcher programs (such as Rofi).

## Configuration

**In progress**

## Installation 

First, you need to download the .zip file and extract the 4 files mentions before (see Composition section).
Then, there is two possibilities :

1) Use the installer programm

Simply run :
$ sudo bash update

The update program will install the files in the right place

2) Manually

Move the bgutc file to /usr/bin/ then run :
$ sudo chmod +x /usr/bin/bgutc

Move the bgutc.conf file to ~/.config/

Move the bgutc.desktop to ~/.local/share/applications/

## If you have an issue

Just, tell me. I'll try to fix as soon as I can.