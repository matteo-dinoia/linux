# Quick Fixes
## To add
reflector how


## Sddm
### WRONG LAYOUT SDDM
```sh
localectl set-x11-keymap --no-convert "it"
localectl set-keymap it
```
### NO SDDM THEMING
pacman -S sddm-kcm
SCREENSHOT
spectacle -rbnc
->tolgo "ignore image"

## Settings
### NO OSD (ON-SCREEN DISPLAY)
* System Settings > Workspace Behavior > General Behavior
* Check: Display visual feedback for status change
### REMOVE MIDDLE CLICK PASTE (ONLY WAYLAND)
* System Settings > Workspace Behavior > General Behavior
* Unceck: Middle click > Paste Selected Text
### NOT ALL ACCOUNT IN ACCOUNT PAGE
```sh
pacman -S kaccounts-providers kio-gdrive
```
### TOO MUCH OPTION IN TOUCHPAD (NOT EVEN WORKING)
remove package synaptics





