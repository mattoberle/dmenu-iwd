# dmenu-iwd

Connect to wireless networks via `dmenu`.

### Features

- Networks sorted by signal strength
- Notifications via `dunst`
- Password entry via `dmenu`

### Requirements

- [`dmenu`](https://wiki.archlinux.org/title/dmenu)
- [`dunst`](https://wiki.archlinux.org/title/Dunst)
- [`iwd`](https://wiki.archlinux.org/title/iwd)
- A user in the `netdev` or `wheel` group

### Installation

Download the script and place it somewhere on your `$PATH`, eg.

```sh
curl https://raw.githubusercontent.com/mattoberle/dmenu-iwd/main/dmenu-iwd >~/bin/dmenu-iwd
chmod +x ~/bin/dmenu-iwd
```

### i3 Integration

Choose a key combination to bind in `~/.config/i3/config`.

Run `i3reload` after to activate the binding.

```
bindsym $mod+n exec --no-startup-id dmenu-iwd
```

### Customization

Edit any of the following values.

```sh
STATION="wlan0"
FONT="Monospace"
NORMAL_BACKGROUND="#000000"
NORMAL_FOREGROUND="#8f8f8f"
SELECTED_BACKGROUND="#000000"
SELECTED_FOREGROUND="#00ff00"
```

Remove `"-b"` from the `FLAGS` array to move the menu to the top.
