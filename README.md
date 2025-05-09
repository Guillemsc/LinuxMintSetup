# LinuxMintSetup

# Theming
- Find Themes app, and select Papirus-Dark for icons, and DMZ-Black for pointer.
- Set bottom bar icons to the center.

# Rofi
- Install through the terminal with `sudo apt install rofi`.
- Copy the rofi folder from this repo into `~/.config/`
- Go to Keyboard app, Shortcuts, Add custom shortcut. Add shortcut `rofi -show drun` with `Super + R`

# Filesystem
- Install Thunar through the package manager.

# Misc
- Find Keyboard app, and turn on Enable key repeat toggle.
- At the bottom bar, pinned Thunar, Terminal, Vivaldi, Spotify and Bitwarden.
- Find Sound app, Sounds, and disable Showing notification sound.

# Development
- Install SmartGit by downloading the program, and placing it on `~/`. Then add it as launcher app. 
- Install git with `sudo apt-get install git`.
- Create `~/.local/share/unity3d/` for unity to work properly.

# Steam
- To enable proton, go to Steam, Settings, Compatability, and enable the toggle Steam Play for all the titles.
- Available games: [https://www.protondb.com/app/3241660](https://www.protondb.com/app/3241660).

# Adding Launcher Apps
- Go to `~/.local/share/applications/`.
- Create a file named `myapp.desktop`.
- Paste this adjusting for the paths:
```
[Desktop Entry]
Version=1.0
Type=Application
Name=My App
Exec=/home/yourusername/path/to/your-app.sh
Icon=/home/yourusername/path/to/icon.png
Terminal=false
Categories=Utility;
```
- Run the newly created `myapp.desktop` file.
- Log out and back in, or un this to refresh immediately: `update-desktop-database ~/.local/share/applications`.

# Local Network Folder Sharing
- Install samba on all machines
- On hosting machine, at `etc/samba/smb.config` add this:
```
[Shared]
path = /home/guillem/Shared
browseable = yes
read only = no
guest ok = yes
```
- Look for hosting machine ip with command `ip a | grep inet`.
- On machines that want to join, on the file explorer path, look for `smb://machineip/Shared/`.


