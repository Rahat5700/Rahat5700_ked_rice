> All credits go to the original creators — I only arranged and combined them.

<img width="1920" height="1080" alt="Desktop Preview" src="https://github.com/user-attachments/assets/e39214c4-46e5-4059-9371-c716fe11e9e1" />

---
## Requirements

Before getting started, install the **Catppuccin Macchiato Lavender** theme from the following the code:

```bash
 https://github.com/orangci/walls-catppuccin-mocha/tree/master
```
```bash
 https://github.com/catppuccin/catppuccin
```
Then you have to install it

[klassy](https://github.com/paulmcauley/klassy)

### emptySession
```bash
kwriteconfig6 --file ksmserverrc --group General --key loginMode emptySession
```
### virtual desktop
You can tell KDE's window manager (KWin) to stop letting applications switch your virtual desktop automatically.
```besh
kwriteconfig6 --file kwinrc --group Windows --key SeparateWidgets true
kwriteconfig6 --file kwinrc --group Windows --key FocusStealingPreventionLevel 3
qdbus6 org.kde.KWin /KWin reconfigure
```



---
## Installation

### Icon Pack

- Download the icon pack from my GitHub and install it:

**[gruvbox-plus-icon-pack.6.4.0.tar.gz]**

### Panel Clock Widget

- Download the widget from my GitHub and install it:

**[local-utc-time-widget.plasmoid]**

### Shortcuts

- Import the shortcut profile:

**[shortcut-pro.kksrc]**

---

## Tiling Manager Configuration

To prevent KWin from conflicting with your tiling manager, run the following commands:

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

---

## Additional Settings

A video walkthrough covering the remaining settings will be provided soon.
