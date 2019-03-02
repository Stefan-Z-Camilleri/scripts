# Fix Mouse Wheel on Linux / X11

## Purpose

This script makes the mouse wheel speed configurable on X11 servers.  

Executing the script will pop-up a dialog that will ask you what speed you'd like to set the mouse wheel to.

## Dependencies

This script requires the following to be installed (using your package manager apt, zypper, yum, etc...)

* imwheel
* zenity

## Usage

1. Download the script
2. `chmod +x fixwheel.sh`
3. ./fixwheel.sh

**Note that the value in the popup indicates granularity, so the higher the value, the slower the scroll.**

## Known Side-effects

This script 'may' kill the back and forward buttons on your mouse.  This is due to a variance of the `imwheel` binary on some distros (ex. Ubuntu 14.04).

If this happens, try replacing the last code line on the script from `imwheel --kill -b 45` to `imwheel --kill -b "4 5"` instead.