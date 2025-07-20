archinstall - desktop hyprland
<br>
audio - pipewire
<br>
DONT use network manager
```
RUN THIS TO PREVENT HANGUP AT BOOT (for like docker service but maybe for smth else as well)

sudo systemctl disable systemd-networkd-wait-online.service
sudo systemctl mask systemd-networkd-wait-online.service
```
```
/etc/iwd/main.conf
[General]
EnableNetworkConfiguration=true
```
[yay install](https://github.com/Jguer/yay?tab=readme-ov-file#installation)
```
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```
Install packages
```
yay -S rustup nodejs npm unzip ripgrep fd wl-clipboard typescript nano nautilus fuzzel zsh uwsm dbus-broker waybar pavucontrol pipewire-pulse wireplumber brightnessctl polkit gnome-keyring libsecret ttf-meslo-nerd-font-powerlevel10k noto-fonts noto-fonts-emoji noto-fonts-cjk noto-fonts-extra ttf-jetbrains-mono
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
<br>
Systemd services
```
systemctl enable systemd-homed --now
systemctl enable systemd-resolved --now
```
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
GNOME Keyring<br>
[PAM](https://wiki.archlinux.org/title/GNOME/Keyring#PAM_step)<br>
[User pass](https://wiki.archlinux.org/title/GNOME/Keyring#Automatically_change_keyring_password_with_user_password)<br>
<br>
## [FNM Install](https://github.com/Schniz/fnm?tab=readme-ov-file#using-a-script-macoslinux)
```
Ensure these params are being used for fnm (.zshrc) 
--use-on-cd --version-file-strategy=recursive --resolve-engines
```
NPM Packages (Install for the fnm use system profile)
```
npm i -g eslint_d prettierd jsonlint markdownlint
```
For NodeJS Provider (MUST DO THIS FOR ALL USED NODEJS VERSIONS)
```
npm i -g neovim
```
Remove NEOVIM & VIM from app launcher (SET noDisplay=true for .desktop files)
