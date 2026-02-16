# riftduma-config

My [rift](https://github.com/acsandmann/rift) tiling window manager config for macOS.

## Setup

```bash
# symlink to rift config directory
mkdir -p ~/.config/rift
ln -sf "$(pwd)/config.toml" ~/.config/rift/config.toml
```

Rift picks up changes automatically via `hot_reload = true`.

## Layout

BSP with 10px outer gaps and 8px inner gaps. Focus follows mouse.

## Keybinds

All bindings use vim-style `hjkl` with arrow key alternatives.

### Window management

| Key | Action |
|---|---|
| `Alt + hjkl/arrows` | Focus window |
| `Alt+Shift + hjkl/arrows` | Swap window |
| `Ctrl+Alt + hjkl/arrows` | Resize window |
| `Ctrl + X` | Toggle float |
| `Alt+Shift + Space` | Toggle float (alt) |
| `Alt+Shift + M` | Toggle fullscreen |
| `Alt + F` | Fullscreen within gaps |
| `Alt + O` | Toggle split orientation |

### Workspaces

| Key | Action |
|---|---|
| `Ctrl + H/L` | Switch macOS space left/right |

Uses native macOS spaces via AppleScript key simulation.

### App launchers

| Key | App |
|---|---|
| `Alt + Q` | Ghostty |
| `Alt + C` | VS Code |
| `Alt + S` | Spotify |
| `Cmd + B` | Zen Browser |
| `Cmd + Enter` | Finder |

### Scratchpad

`Cmd+Shift + T` toggles a floating Ghostty terminal titled "scratchpad". First press launches it, subsequent presses hide/show it via `AXMinimized`. The window auto-floats via an `app_rules` title match.

### Other

| Key | Action |
|---|---|
| `Ctrl+Alt + M` | Mission control (all spaces) |
| `Ctrl+Alt+Shift + M` | Mission control (current space) |
| `Alt+Shift + D` | Debug |
| `Ctrl+Alt + Q` | Save and exit rift |

## Modifier aliases

Defined in `[modifier_combinations]` for cleaner keybind syntax:

- `shift_alt` = `Alt + Shift`
- `ctrl_alt` = `Alt + Ctrl`
- `ctrl_alt_shift` = `Alt + Ctrl + Shift`

## Companion tools

- [Easy Move+Resize](https://github.com/dmarcotte/easy-move-resize) for `Cmd+drag` to move and `Cmd+right-drag` to resize windows alongside rift
