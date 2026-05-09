All credits go to the original creators — I only arranged and combined them.
<img width="1920" height="1080" alt="Screenshot_২০২৬০৫০৯_১১২০২৪-1" src="https://github.com/user-attachments/assets/e39214c4-46e5-4059-9371-c716fe11e9e1" />

1st you need to install
CatppuccinMacchiatoLavender
```bash
https://github.com/orangci/walls-catppuccin-mocha/tree/master
```
```bash
https://github.com/catppuccin/catppuccin
```
#Then you need to install the icon pack
You can download the file from my GitHub
**[gruvbox-plus-icon-pack.6.4.0.tar.gz]**

#For the panel clock 
You need to download the widget from my GitHub
**[local-utc-time-widget.plasmoid]**

#I have some simple shortcut 
**[shortcut pro.kksrc]**

#For better tiling you need to change some settings
```bash
# 1. Disable the "Scale" and "Maximize" animations (the main cause of flickering)
kwriteconfig6 --file kwinrc --group Plugins --key scaleEnabled false
kwriteconfig6 --file kwinrc --group Plugins --key maximizeEnabled false
# 2. Set Window Placement to "No Placement"
# This stops KWin from trying to position the window before your Tiling Manager takes over.
kwriteconfig6 --file kwinrc --group Windows --key Placement 0
# 3. Prevent KWin from remembering and restoring old window sizes
kwriteconfig6 --file kwinrc --group Windows --key GeometryRestore false
# 4. Tell KWin to reload the configuration immediately
qdbus6 org.kde.KWin /KWin reconfigure
echo "Done! KDE should now stop fighting your tiling manager."
```
I will give a video which will show my rest of the settings
