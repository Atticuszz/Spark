

## 1. APT (Advanced Package Tool)

### Basic Usage

- Update package list: `sudo apt update`
- Upgrade all packages: `sudo apt upgrade`
- Install software: `sudo apt install <package-name>`
- Uninstall software: `sudo apt remove <package-name>`
- Search for software: `apt search <keyword>`
- Display package information: `apt show <package-name>`

### Principles
APT is an advanced package management tool that uses dpkg as its backend. APT can:
- Resolve dependencies
- Fetch packages from configured sources
- Perform complex package management operations

### PPA Configuration
PPA (Personal Package Archive) allows developers and users to create their own software repositories.

- Add PPA: `sudo add-apt-repository ppa:<repository-name>`
- Remove PPA: `sudo add-apt-repository --remove ppa:<repository-name>`

PPA source files are located in the `/etc/apt/sources.list.d/` directory.

## [Deb-Get](https://github.com/wimpysworld/deb-get)

Deb-Get is a tool for installing `.deb` packages, particularly useful for obtaining software from platforms like GitHub.

### Installing Deb-Get
```bash
sudo apt install curl lsb-release wget
curl -sL https://raw.githubusercontent.com/wimpysworld/deb-get/main/deb-get | sudo -E bash -s install deb-get
```

### Configuring GitHub PAT (Personal Access Token)
1. Create a PAT on GitHub: Settings > Developer settings > Personal access tokens
2. Set environment variable:
   ```bash
   echo 'export GITHUB_TOKEN=your_token_here' >> ~/.zshrc
   source ~/.zshrc
   ```

### Basic Usage
- Search for software: `deb-get search <package>`
- Install software: `sudo deb-get install <package>`
- Update all software: `sudo deb-get update-all`

## 3. Flatpak

Flatpak is a system for building and distributing desktop applications.

### Installing Flatpak
```bash
sudo apt install flatpak
```

### Adding Flathub Repository
```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

### Basic Usage
- Search for apps: `flatpak search <app-name>`
- Install apps: `flatpak install <app-id>`
- Run apps: `flatpak run <app-id>`
- Update all apps: `flatpak update`
- Uninstall apps: `flatpak uninstall <app-id>`

### Automatic Updates
Flatpak can be configured for automatic updates:
1. Install GNOME Software: `sudo apt install gnome-software-plugin-flatpak`
2. Enable automatic updates in GNOME Software

Or set up periodic updates using command line:
```bash
flatpak update --appstream
flatpak update
```
These commands can be added to a cron job for automatic updates.
