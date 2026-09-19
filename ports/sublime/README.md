# Sublime Text

Original Midnight Aurora Subtle files, copied from the current Sublime Text User package.

| File | Role |
|------|------|
| `Midnight Aurora Subtle.sublime-color-scheme` | Syntax colors (current ST color scheme) |
| `Midnight Aurora.sublime-theme` | Matching UI chrome (sidebar, tabs, status bar) |

The live Sublime setup may pair this color scheme with a different UI theme (for example Zed Dark). This port keeps the Aurora UI theme next to the scheme so the pair stays in the repo.

## Install

Copy into `~/Library/Application Support/Sublime Text/Packages/User/`:

```sh
cp -p "Midnight Aurora Subtle.sublime-color-scheme" \
  "$HOME/Library/Application Support/Sublime Text/Packages/User/"
cp -p "Midnight Aurora.sublime-theme" \
  "$HOME/Library/Application Support/Sublime Text/Packages/User/"
```

Then in Preferences:

```json
"color_scheme": "Midnight Aurora Subtle.sublime-color-scheme"
```
