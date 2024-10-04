<div align="center">
    <h1>【 Modified from end_4's Dotfiles 】</h1>
    <h3></h3>
</div>

<div align="center">
    <h2>• Arch Install •</h2>
</div>

- Mirror Region (Estonia)
- Drive Formatting (ext4)
- Profile (Minimal)
- Audio (PipeWire)
- Kernel (Linux)
- Additional Packages (curl)
- Network (NetworkManager)
- Timezone (Europe/Tallinn)
- Optional Repositories (multilib)

<div align="center">
    <h2>• Rice Install •</h2>
</div>

- **Automatic**, but guided and transparent, installation for Arch(-based) Linux:

```bash
bash <(curl -s "https://raw.githubusercontent.com/Krayon0/dotfiles/refs/heads/master/setup.sh")
```

<div align="center">
    <h2>• Apps Requiring Manual Install •</h2>
</div>

- Vesktop
    - `flatpak install flathub dev.vencord.Vesktop`
- Yubico Authenticator
    - `yay -S yubico-authenticator-bin`

<div align="center">
    <h2>• NVIDIA Guide •</h2>
</div>

- https://wiki.hyprland.org/Nvidia/
- Install 'nvidia' & 'nvidia-utils' & 'lib32-nvidia-utils' & 'egl-wayland'
    - Follow the DRM & ENV Parts
- Read through the rest and apply the changes (DRM, ENV, VA-API, Flickering, etc.)

<div align="center">
    <h2>• Credits •</h2>
</div>

- https://github.com/end-4/dots-hyprland
