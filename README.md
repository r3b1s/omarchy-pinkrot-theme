# Omarchy pinkrot theme

pinkrot is a near-black, red-tinted theme: crimson chrome on a `#050007`
surface, a warm pink foreground, and `#d40d40` as the accent. It is the Omarchy
port of the `pinkrot` theme from
[athena-dots](https://github.com/r3b1s/athena-dots).

## Preview

![pinkrot theme preview](preview.png)

## Install

```bash
omarchy theme install https://github.com/r3b1s/omarchy-pinkrot-theme
```

The repo is named `omarchy-pinkrot-theme`, so it installs as **pinkrot** and
appears as *Pinkrot* in the theme switcher.

## Palette

`colors.toml` is the source of truth. Chrome stays crimson; the syntax colours
are pinkrot's own editor palette, so terminals and editors get distinguishable
hues without leaving the red/pink family.

| Role | Key | Value |
| --- | --- | --- |
| Accent | `accent` | `#d40d40` |
| Selection | `selection` / `selection_foreground` | `#d40d40` / `#050007` |
| Background | `background` | `#050007` |
| Surface | `lighter_background` | `#0d060b` |
| Foreground | `foreground` | `#f17e97` |
| Bright foreground | `bright_foreground` | `#ffd6df` |
| Muted | `muted` | `#8f4d61` |
| Red | `red` | `#ff365f` |
| Orange | `orange` | `#ff7a45` |
| Yellow | `yellow` | `#ffc05a` |
| Green | `green` | `#9dd274` |
| Cyan | `cyan` | `#7fd6d4` |
| Blue | `blue` | `#7a89ff` |
| Magenta | `magenta` | `#ff4f7a` |

Window borders (`hyprland_active_border`, `hyprland_inactive_border`) carry the
pinkrot red ramp as a gradient, which Omarchy feeds to Hyprland and the shell.

### Monochrome terminal

pinkrot's Athena terminal is a single-hue red ramp. Omarchy drives terminals
from the same semantic keys as everything else, so a coloured terminal is the
default here. `colors.toml` ends with a commented block that restores the
monochrome ramp; uncomment it and re-apply the theme if you want the original
terminal look back, accepting red-toned syntax highlighting as the trade.

## What's included

| File | Purpose |
| --- | --- |
| `colors.toml` | The palette; drives every generated config |
| `backgrounds/` | `0-bleach.webp` plus the `omarchy.webp` fallback |
| `unlock.png` / `preview-unlock.png` | Lock screen art (Style > Unlock) |
| `preview.png` | Theme switcher preview |
| `btop.theme` | pinkrot btop colours |
| `chromium.theme` | Chromium background (`5,0,7`) |
| `icons.theme` | `Yaru-red` |
| `keyboard.rgb` | Keyboard backlight colour (`#d40d40`) |

No terminal config, Lua, or `vscode.json` is shipped. Omarchy regenerates those
from `colors.toml` anyway, and drops them from a theme installed out of a git
repo, so the repo only carries files that survive installation.

## Notes

- `foreground` is the Athena terminal pink (`#f17e97`); `bright_foreground` is
  the brighter editor foreground (`#ffd6df`) used for cursors and bright text.
- Additional wallpaper for this theme goes in
  `~/.config/omarchy/backgrounds/pinkrot/`; it is not tracked here.
