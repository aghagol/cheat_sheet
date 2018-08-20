Force alt + tab to switch only on current workspace in GNOME shell

```bash
gsettings set org.gnome.shell.app-switcher current-workspace-only true
```

GNOME Tweak Tool

```bash
sudo apt install gnome-tweak-tool
```

---
Fix Alt-tab to switch between windows instead of apps:

- Open `dconf-editor`
- Go to `org/gnome/desktop/wm/keybindings`
- Move the value `'<Alt>Tab'` from `switch-applications` to `switch-windows`
- Optionally move `'<Shift><Alt>Tab'` from `switch-applications-backward` to `switch-windows-backward`
- If you want `switch-windows` to work across desktops, not just in the current desktop, you can also uncheck `org/gnome/shell/window-switcher/current-workspace-only` (Courtesy of @CharlBotha)
- Close `dconf-editor`
- Press `<Alt>F2`, then type `r` to restart Gnome.

The last step does not always appear to be necessary, but it should not hurt (especially since it does not close any of your running applications).

---
