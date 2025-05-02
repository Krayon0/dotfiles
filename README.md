archinstall - desktop hyprland<br>
audio - pipewire<br>
use networkmanager - nmcli<br>

[yay install](https://github.com/Jguer/yay?tab=readme-ov-file#installation)
```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```
[zsh install](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
<br>
`sudo pacman -S zsh`<br>
`chsh -s /usr/bin/zsh`<br>
<br>
[ohmyzsh install](https://github.com/ohmyzsh/ohmyzsh?tab=readme-ov-file#basic-installation)
<br>
install font for powerlevel10k - `yay -S ttf-meslo-nerd-font-powerlevel10k`
<br>
<br>
[install powerlevel10k](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#manual)
<br>
`exec zsh`
<br>
<br>
Autostart Hyprland
```
if uwsm check may-start; then
  exec uwsm start hyprland-uwsm.desktop
fi
```
