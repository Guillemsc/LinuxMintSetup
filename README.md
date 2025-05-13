# LinuxMintSetup

# Theming
- Find Themes app, and select `Papirus-Dark` for icons, and `DMZ-Black` for pointer.
- Set bottom bar icons to the center.
- Right click on the Menu icon, Configure, Icon, and select `start-here-symbolic`.
- Right click on the bottom bar, Panel Settings, Right Zone, and select 16px for colored icon size and symbolic icon sizes.

# Rofi
- Install through the terminal with `sudo apt install rofi`.
- Copy the rofi folder from this repo into `~/.config/`.
- Go to Keyboard app, Shortcuts, Add custom shortcut. Add shortcut with command `rofi -show drun` and key `Super + R`.

# Filesystem
- Install Thunar through the package manager.

# Screenshot
- Install Flameshot through the package manager.
- Set it to run at startup.
- Add shortcut with command `flameshot gui` and key `Print`.

# Terminal
- Open therminal, left click, preferences.
- On Shortcuts, change them so they don't use shift.
- On Colors, Palette, select GNOME.
- On the Keyboard app, modify the shortcut `Launch terminal`, to `Super + T`.

# Keyboard
- Find Keyboard app, and turn on Enable key repeat toggle.

# Misc
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
- Install samba on all machines.
- On hosting machine create shared folder with appropiate permissions, with `chmod 755 /home/<YOUR_USERNAME>` and `chmod 777 /home/<YOUR_USERNAME>/Shared`.
- On hosting machine, at `etc/samba/smb.config` add this:
```
[Shared]
path = /home/guillem/Shared
browseable = yes
read only = no
guest ok = yes
```
- Look for hosting machine ip with command `ip a | grep inet`.
- On machines that want to join, on the file explorer path, look for `smb://<MACHINE_IP>/Shared/`.
- After that, bookmark the shared folder on the file explorer.


