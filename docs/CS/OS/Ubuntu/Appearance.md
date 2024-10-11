# Appearance

## Theme

[GitHub - vinceliuice/WhiteSur-gtk-theme: MacOS Big Sur like theme for Gnome desktops](https://github.com/vinceliuice/WhiteSur-gtk-theme)

### Basic Extension

- [user-themes](https://extensions.gnome.org/extension/19/user-themes/) to enable gnome-shell theme (and not just the application theme)
- [dash-to-dock](https://extensions.gnome.org/extension/307/dash-to-dock)
- [blur-my-shell](https://extensions.gnome.org/extension/3193/blur-my-shell)

### Install

```bash
git clone git@github.com:vinceliuice/WhiteSur-gtk-theme.git
cd WhiteSur-gtk-theme
./install.sh --libadwaita \
--monterey \
-c Dark \
-t blue \
--gnome-shell \
--round \

sudo flatpak override --filesystem=xdg-config/gtk-3.0 && sudo flatpak override --filesystem=xdg-config/gtk-4.0

./tweaks.sh -F \
-f \
--dash-to-dock \
--color Dark \
--theme blue


```

### Tweak

Firefox theme

```bash
./tweaks.sh -f
```

## Icons

[GitHub - vinceliuice/WhiteSur-icon-theme: MacOS Big Sur style icon theme for linux desktops](https://github.com/vinceliuice/WhiteSur-icon-theme)

```bash
git clone git@github.com:vinceliuice/WhiteSur-icon-theme.git
cd WhiteSur-icon-theme 
./install.sh -a -b
```

## Cursors

```bash
git clone git@github.com:vinceliuice/McMojave-cursors.git
cd McMojave-cursors
sudo ./install.sh
```
