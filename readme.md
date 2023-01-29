# My Fedora Installation

### Screenshot
![SS](https://github.com/BIBJAW/fedora_stuffs/blob/main/Fedora.png)

## Rice : 
```
 git clone https://github.com/BIBJAW/fedora_stuffs && chmod +x ~/fedora_stuffs/fedora_configs/i3/scripts/powermenu && chmod +x ~/fedora_stuffs/fedora_configs/polybar/launch.sh
 ```
 #### Original Rice: https://github.com/BIBJAW/Final_Rice

## After the base :

**1. Drivers:**

- xorg-x11-drv-amdgpu 

- xorg-x11-drv-ati

- mesa-vulkan-drivers

- vulkan-headers

- vulkan-loader

**2. Basic System packages:**

- @base-x 

- neovim

- lightdm

- slick-greeter

- dejavu-fonts-all

- i3

- i3lock

- polybar 

- rofi

- alacritty

- pcmanfm

- gvfs

- gvfs-mtp

- gvfs-gphoto2

- simple-mtpfs

- jmtpfs 

- ntfs-3g

- mate-polkit 

- xarchiver 

- unzip

- unrar

- flameshot

- lxappearance

- nitrogen

- htop

- lm_sensors

- git 

- wget 

- curl

- tar

- cmake 

- gcc

- ibus

- picom

- network-manager-applet

- NetworkManager-wifi

- iw

- wireless-regdb

- wpa_supplicant

- xset

- xdg-utils

- xdg-desktop-portal 

- xdg-desktop-portal-gtk

- xdg-user-dirs

- dbus

- dbus-common

- dbus-daemon

- dbus-devel

- dbus-doc

- dbus-libs

- dbus-tests

- dbus-tools

- dbus-x11

- pipewire

- pipewire-pulseaudio

- pipewire-jack-audio-connection-kit

- pavucontrol

- musikcube

- mingw64-gcc

- gcc-c++

- java-latest-openjdk

**3. GUI Apps:**

- firefox

- qBittorrent

- atril

- feh

- mpv


- gnome-disk-utility

- gnome-keyring

- libgnome-keyring

- vscode

- libreoffice

- libreoffice-gtk3

- marktext

- gimp

- simplescreenrecorder

- discord

- slack

- telegram


### Post installation :
** RPM Fusion: **
``` 
sudo dnf install \
  https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm
  
sudo dnf install \
  https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
  ```
  
  ** Multimedia Codecs **
  ```
sudo dnf install gstreamer1-plugins-{bad-\*,good-\*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel

sudo dnf install lame\* --exclude=lame-devel

sudo dnf groupupdate multimedia --setop="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin

sudo dnf groupupdate sound-and-video

sudo dnf group upgrade --with-optional Multimedia
  
  ```

** MS Fonts **

```
sudo dnf upgrade --refresh -y

sudo dnf install curl cabextract xorg-x11-font-utils fontconfig -y

sudo rpm -i https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm
```




























