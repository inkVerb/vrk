# Vrk
Supercharge your Manjaro desktop

## Supported Environments
- Xfce
- GNOME

### Hotkeys & Desktop:
- Move window: <key>Alt</key> + click anywhere
- Scale window: <key>Alt</key> + right click near edge or corner
- Dropdown terminal: <key>F12</key> (<key>Scroll Lock</key>?)
- Volume mute: <key>Shift</key> + <key>Pause</key>
- Volume up: <key>Shift</key> + <key>Page Up</key>
- Volume down: <key>Shift</key> + <key>Page Down</key>

### GNOME Actions:
- Compose: <key>CapsLock</key>
- Activities: Top left corner mouse; <key>Super</key>
- Applications: <key>Ctrl</key> + <key>Left Super</key>
- Switch workspaces: <key>Ctrl</key> + <key>Alt</key> + <key>Left</key>/<key>Right</key>
- New window: middle click on menu's app icon
- Minimize: middle click on title bar

### Xfce Hotkeys:
<key>Super</key> opens the menu.
<key>Ctrl</key> + <key>Super</key> + <key>Up</key>/<key>Down</key>/<key>Right</key>/<key>Left</key> tiles your window in 1/2 screen.
<key>Shft</key> + <key>Super</key> + <key>Up</key>/<key>Down</key>/<key>Right</key>/<key>Left</key> tiles your window in 1/4 screen on the top.
<key>Alt</key>  + <key>Super</key> + <key>Up</key>/<key>Down</key>/<key>Right</key>/<key>Left</key> tiles your window in 1/4 screen on the bottom.
<key>Ctrl</key> + <key>Super</key> + <key>Alt</key> shows your window spread & dashboard.
Scroll on the desktop to switch workspaces.

# What is Vrk?
- A collection of simple scripts for tools and settings
- The installer adds many apps, settings, and special Vrk shell scripts, including scripts that make SSH, Git, and FileZilla easier to integrate.
- A hidden folder will be created in home: `.vrk`
- Scripts are in `.vrk/boards`

## How to Install

```console
git clone https://github.com/inkVerb/vrk
cd /vrk/inst
chmod ug+x govrk
sudo ./govrk $DESKTOP_SESSION
```

- Answer the two simple folder questions carefully
- The machine will reboot if you are installing the first time.

### Other Users
For a user that will not have boss/ folder permissions:

`sudo install-vrk user`

For a a user to have boss/ folder permissions:

`su SOMEUSER`

`cd /opt/vrk/boss`

`sudo ./install-vrk`

`exit`

### Updates
- If already installed, the same install procedure will update instead.
- Some specific features per user must be updated per user.
- This will update the core and all users:

`cd /vrk/inst`

`chmod ug+x upvrk`

`sudo ./upvrk $DESKTOP_SESSION`

# Developer info

## File hierarchy
- `~/.vrk`:

1. `boards` lists the Vrk scripts you can use, tools to manage your system. Most of these are global and you can run them from any terminal.
2. `configs` has stuff you only want to touch if you don't mind messing up everything and really want to learn how Vrk works.
3. `donjon` has stuff that Bosses need, generally don't mess. But, there are some hidden goodies in there if you aren't afraid of the dragons.
4. `go` has your quick scripts that let you SSH your way into remote servers very quickly and control them from the command line.
   *Add "Go Surfers" by following the instructions in the "Go Surfers" instructions.*

- `/opt/vrk` is where the actual files and other assets exist, such as may useable in `$PATH`

## Vrk Cloud
- This puts Work folder, Documents, Templates (GNOME) in a cloud folder of your choice
- Install it from `sudo install-vrk-cloud` or `sudo install-vrk-cloud user`

## Different installs
- `install-mi-dev`: Desktop settings, plus tools for developers
- `install-mi-basic`: Desktop settings, plus tools for artists
- `install-mi-all`: All of the above

## Other Vrk tools
- Manage SSH profiles & FileZilla integration `surf/ssh-*`
- OpenVPN based on SSH profile `surf/vpn-add`
- GitHub streamlined for simple use `surf/vgit*`
- Vrk installation info via `vinf`
- Recursive directory `sed` replacements via `vsed`
- `tar` & `xz` a directory via `vtar`

## Hierarchies
- Some commands are included in other commands
- Understand these for the `boss/` and `surf/` folders in `vrk/hierarchies`

## Droids
- Droids are located in `/opt/vrk/droids/USER/`.
- Droids located in `/opt/vrk/droids/ALL/` can be used by all users.
- Droids are not changed or removed with an update and you can add them yourself.

## More settings and information at [Manjaro in Style](https://github.com/inkVerb/Mi)
- Change some settings on the back end
- Implement many settings for CentOS GNOME
