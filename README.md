# RetroPie-Xubuntu

This is my attempt at making a clean & easy way to take a vanilla Xubuntu installation and create a dedicated RetroPie system.
The goal is to make this as close to the standard RetroPie install on a Raspberry Pi as possible.

# Why Xubuntu?

* Official alternate for Ubuntu's standard desktop
* Incredibly light-weight
* Very straight-forward UI
* Easy to customize with built-in tools

# Steps

## Installing Xubuntu

* Download & install [Xubuntu 22.04 LTS](https://cdimage.ubuntu.com/xubuntu/releases/focal/release/) which will be supported until 2025
  * During the installation, ensure you set to have your user automatically log-in
  * Choose whatever username you'd like, my configuration script isn't dependent on the '''pi''' username

## Running My RetroPie Script

Clone this repository & run the script

```
git -C $HOME clone https://github.com/xovox/RetroPie-Xubuntu/
cd $HOME/RetroPie-Xubuntu
chmod +x retropie_xubuntu
./retropie_xubuntu
```

The script will perform the following

* Disable desktop compositing
* Disable screen power-down
* Power button now shuts down the system immediately
* Disable hibernation/sleep
* Set a dark theme
* Upgrade the OS & install required packages
* Enable passwordless sudo for your user
* Download, compile & configure RetroPie
* Replace lr-mame2003 with lr-mame2003-plus
* Replace mupen64plus with lr-mupen64plus
* Install Intellivision, Neo Geo CD, MSX emulators
* Install scraper
* Enable auto-start

## Disabling Auto-Start

Open up a terminal and run the following

```
rm $HOME/.config/autostart/retropie.desktop
```
