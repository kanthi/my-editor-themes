# Ghostty

Ghostty terminal themes for the Midnight Aurora family. One file per variant, colors mapped from `palettes/midnight-aurora-*.json`.

| File | Theme |
|------|-------|
| `midnight-aurora-subtle` | Original navy |
| `midnight-aurora-void` | Near-black |
| `midnight-aurora-dusk` | Lifted navy |
| `midnight-aurora-ember` | Warm dark |
| `midnight-aurora-tide` | Cool blue-black |
| `midnight-aurora-haze` | Warm stone, lowest contrast |

## Install

```sh
mkdir -p "$HOME/.config/ghostty/themes"
cp -p "$HOME/Workspace/Repos/my-editor-themes/ports/ghostty/"midnight-aurora-* \
  "$HOME/.config/ghostty/themes/"
```

In `~/.config/ghostty/config`:

```
theme = midnight-aurora-haze
```

Reload Ghostty. Theme lookup uses `~/.config/ghostty/themes` by filename.

Do not invent hex here. Map from `palettes/midnight-aurora-*.json`.
