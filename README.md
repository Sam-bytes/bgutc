# Bash Graphical User Theme Changer (bgutc)

bgutc is a bash script that allows for quick switching between different theming presets.

## Installation

* TBD

## Configuration


### Step 1: Add programs to the config
On the **first** line of the configuration file, add the names of the programs whose themes you want to switch:

---
> ~/.config/bgut.conf
```
rofi waybar
```
---
### Step 2: Add presets to your config

On the **second** line, add the names of your themes:

---
> ~/.config/bgut.conf
```
rofi polybar
waterfall nightfall
```
---
### Step 3: Preset Creation

---
You now have to provide the path to each program's configuration files, for each preset:
> ~/.config/bgut.conf
```
[program's name]
conf="/path/to/the/default/config/file"
preset_1="/path/to/a/preset/file" 
preset_2="/path/to/another/preset/file"
```
---

### Full example:

> ~/.config/bgut.conf
```
rofi polybar
waterfall nightfall

[rofi]
conf="~/.config/rofi/config.rasi
waterfall="~/.config/rofi/waterfall.rasi"
nightfall="~/.config/rofi/config/nightfall.rasi"

[polybar]
conf="~/.config/polybar/config.ini"
waterfall="~/.config/polybar/waterfall.ini"
nightfall="~/.config/polybar/nightfall.ini"
```

## Compatibility:

Currently, bgutc is compatible with:

#### WM's
- i3

#### Bars
- polybar

#### Other
- rofi

## If you have an issue

Just, tell me. I'll try to fix as soon as I can.
