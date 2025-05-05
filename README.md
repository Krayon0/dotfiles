archinstall - desktop hyprland
<br>
audio - pipewire
<br>
use networkmanager - nmcli
<br>
<br>
[yay install](https://github.com/Jguer/yay?tab=readme-ov-file#installation)
```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```
Install packages
```
yay -S nano nautilus fuzzel zsh uwsm dbus-broker waybar pavucontrol pipewire-pulse wireplumber polkit ttf-meslo-nerd-font-powerlevel10k
```
[zsh install](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
<br>
`chsh -s /usr/bin/zsh`
<br>
<br>
[ohmyzsh install](https://github.com/ohmyzsh/ohmyzsh?tab=readme-ov-file#basic-installation)
<br>
<br>
[install powerlevel10k](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh)
<br>
`exec zsh`
<br>
<br>
[install dbus-broker](https://github.com/bus1/dbus-broker/wiki)
```
systemctl enable dbus-broker.service
systemctl --global enable dbus-broker.service
```
[install uwsm](https://wiki.hyprland.org/Useful-Utilities/Systemd-start/)
<br>
Add dotfiles
```
cd ~
git init
git branch -m main
git remote add origin git@github.com:Krayon0/dotfiles.git
git pull
```
Waybar
```
systemctl --user enable --now waybar.service
```
Bugs
<br>
If apps take long to open then enable `systemd-homed` & `systemd-resolved`
