# LinuxMintSetup

# Theming
- Find Themes app, and select Papirus-Dark for icons, and DMZ-Black for pointer.
- Set bottom bar icons to the center.

# Filesystem
- Install Thunar through the package manager.

# Misc
- Find Keyboard app, and turn on Enable key repeat toggle.
- At the bottom bar, pinned Thunar, Terminal, Vivaldi and Bitwarden.
- Find Sound app, Sounds, and disable Showing notification sound.

# Development
- Install SmartGit by downloading the program, and placing it on ~/. 
- Install git with sudo apt-get install git.
- Create ~/.local/share/unity3d/ for unity to work properly.

# Adding launcher apps
- Go to ~/.local/share/applications/
- Create a file named myapp.desktop
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


