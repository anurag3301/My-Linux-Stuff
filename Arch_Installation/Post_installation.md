## The Post installation after Base install
**Login to new user created**

**First enable and start the dhcpcd service**
```sh
sudo systemctl enable --now dhcpcd
```
**Now install some absolute important packages**
```sh
sudo pacman -Sy base-devel git firefox wget nvidia nvidia-settings unzip
```
**Install some display and audio packages**
```sh
# Install the packages
sudo pacman -Sy alsa-utils pulseaudio xorg-server xorg-xinit libx11 libxinerama libxft webkit2gtk

# Start the pulse audio service
systemctl --user enable pulseaudio
```
**Clone my-linux-setup repo, my build of dwm, paru**
```sh
# Cloning my linux-setup.git
https://github.com/anurag3301/my-linux-setup.git

# Cloning my build of dwm
https://github.com/anurag3301/my-dwm.git

# Cloning paru
git clone https://aur.archlinux.org/paru.git
```
**Lets build and install dwm and paru**
```sh
# Install dwm
cd dwm
sudo make clean install

# Install paru
cd paru
makepkg -si
```
**Install the rest of the pacman and aur packages**
```sh
sudo pacman -S bat bpython cmake cmatrix discord dmenu dunst evince exa ffmpeg figlet firefox gcc gimp grep htop imagemagick kitty lolcat maim neofetch nitrogen npm nvtop obs-studio picom playerctl ranger telegram-desktop v4l-utils vlc openssh noto-fonts-emoji python-pillow 

paru -S brave-bin ccrypt spofity visual-studio-code-bin gotop 
```