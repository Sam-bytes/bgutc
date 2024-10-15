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

All configurations must be made in the bgutc.conf file !

### Step 1 : Tell which programs you want to changer their configuration

> For example, I need to change my polybar and my rofi configuration

Write the name of these programs at the **first** line of the file :

---
\# ~/.config/bgutc.conf
rofi polybar

---

### Step 2 : Name your preset

> For example, I have two presets : waterfall and nightfall

Write the name of these presets at the **second** line of the file :

---
\# ~/.config/bgutc.conf
rofi polybar
waterfall nightfall

---

### Step 3 : Write the path

Now, you have to write where the config file (the one which will be read by your program) is and where your config files are by following this structure :

---
\[program_name]
conf="/path/to/the/conf/file"
preset_1="/path/to/your/conf/file1"
preset_2="/path/to/your/conf/file2"

---

In my example, I have to write this :

---
\# ~/.config/bgutc.conf
rofi polybar
waterfall nightfall

\[rofi]
conf="/home/user/.config/rofi/config.rasi"
waterfall="/home/user/.config/rofi/config_waterfall.rasi"
nightfall="/home/user/.config/rofi/config_nightfall.rasi"

\[polybar]
conf="/home/user/.config/polybar/config.ini"
waterfall="/home/user/.config/polybar/config_waterfall.ini"
nightfall="/home/user/.config/polybar/config_nightfall.ini"

---

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

## Compatibility list

Currently, bgutc is compatible with :

- i3
- polybar
- rofi

## If you have an issue

Just, tell me. I'll try to fix as soon as I can.