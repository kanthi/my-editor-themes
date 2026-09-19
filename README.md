# my-editor-themes

Personal editor themes, one palette, many ports.

The first theme is **Midnight Aurora Subtle** — the same colors as the current Sublime Text color scheme, ported to VS Code / Antigravity IDE.

## Layout

```text
palettes/                         shared color tokens (source of truth)
ports/
  vscode/                         VS Code extension (also Cursor, Antigravity IDE)
  antigravity-ide/                install notes for the vscode port
  cursor/                         install notes for the vscode port
  sublime/                        original Sublime Text scheme + matching UI theme
  zed/                            not ported yet
```

Editor-specific files live under `ports/<editor>/`. Do not invent a second palette inside a port — extend `palettes/` first, then map those tokens.

VS Code, Cursor, and Antigravity IDE share the **vscode** port. Those apps load the same `package.json` theme contribution. Extra folders under `ports/` exist so install steps stay per-editor.

## Themes

| Theme | Palette | Ports |
|-------|---------|-------|
| Midnight Aurora Subtle | [palettes/midnight-aurora-subtle.json](palettes/midnight-aurora-subtle.json) | vscode, sublime |

## Install

- [Antigravity IDE](ports/antigravity-ide/README.md)
- [VS Code](ports/vscode/README.md)
- [Cursor](ports/cursor/README.md)
- [Sublime Text](ports/sublime/README.md)

## New editor port

1. Add `ports/<editor>/` with a README that names the palette and the native file format.
2. Map tokens from `palettes/<theme>.json` — do not pick new hex values unless the native format needs an extra UI role, and then add that role to the palette.
3. Link the port from this README.

## License

MIT. See [LICENSE](LICENSE).
