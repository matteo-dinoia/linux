### REMEMBER TO DO
reflector how


### WRONG LAYOUT SDDM
```sh
localectl set-x11-keymap --no-convert "it"
localectl set-keymap it
```


### SCREENSHOT
* Use command in the costum shortcut: ``` spectacle -brenc ```
* clipboard->config->general->non-text-selection->"Only when explecetly copied"

### ONLY OPENDESKTOP (ACCOUNT)
```sh
pacman -S kaccounts-providers
```

### ONLY YT IN GOOGLEACCOUNT (for Google Drive)
```sh
pacman -S kio-gdrive
```

### MAN
```sh
pacman -S man-db man-pages
```

### GREETING FISH
function fish_greeting
end

### NO SDDM THEMING
pacman -S sddm-kcm
SCREENSHOT
spectacle -rbnc
->tolgo "ignore image"


### NO PDF PREVIEW
pacman -S kdegraphics-thumbnailers

### YAKUAKE NOT OPENING FIRST TIME
create costum shorcut


### FIREFOX SLOW
change dns (in ipv4 del wifi)
a     8.8.8.8, 8.8.4.4


### TABLET NOT WORKING PROPERLY
pacman -S xf86-input-wacom
pacman -S usbutils (temporaneo)
lsusb  (e certo tavoletta e codice <4 exa:4 exa>)
sudo nano /etc/X11/xorg.conf.d/50-tablet.conf
(E inserisco:
    Section "InputClass"
        Identifier "Tablet"
        Driver "wacom"
        MatchDevicePath "/dev/input/event*"
        MatchUSBID "INSERISCO CODICE TROVATO PRIMA"
    EndSection
)
pacman -Runsc usbutils
reboot


### SLOW PC
https://www.linkedin.com/pulse/how-make-your-archlinux-faster-sourav-goswami

### SETTING UP SYSTEMD-BOOT
https://www.addictivetips.com/ubuntu-linux-tips/set-up-systemd-boot-on-arch-linux/
file /boot/loader/entries/arch.conf
    title Arch Linux
    linux   /vmlinuz-linux
    initrd /initramfs-linux.img
    options "root=PARTUUID=52c6c8e8-99a9-fa47-8e66-869dfb3b8954 quiet loglevel=3 systemd.show_status=0 rw"
file /boot/loader/loader.conf
    default arch
    timeout menu-hidden
    console-mode auto
    editor no

### NANO NO COLOR
Nano ships with predefined syntax highlighting rules, defined in /usr/share/nano/*.nanorc. To enable them, add the following line to your ~/.config/nano/nanorc or to /etc/nanorc:
include "/usr/share/nano/*.nanorc"

### NANO AS DEFAULT
export VISUAL=nano
export EDITOR=nano

### SET GIT TO USE NANO
git config --global core.editor "nano"

### ADDING PARALLEL DOWNLOAD ON PACMAN/YAY
sudo nano /etc/pacman.conf
uncommnet: ParallelDownloads = 5

### TOO MUCH OPTION IN TOUCHPAD (NOT EVEN WORKING)
remove package synaptics
