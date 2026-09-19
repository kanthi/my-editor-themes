# my-editor-themes

Personal editor themes, one palette, many ports.

**Midnight Aurora** is a family of dark themes. **Subtle** matches the current Sublime Text color scheme. Void, Dusk, Ember, and Tide keep the same syntax roles with different dark backgrounds and small accent shifts.

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

| Theme | Background | Shift | Ports |
|-------|------------|-------|-------|
| Midnight Aurora Subtle | `#0e1319` navy | original | vscode, sublime |
| Midnight Aurora Void | `#080b0f` near-black | muted accents | vscode |
| Midnight Aurora Dusk | `#161c26` lifted navy | brighter chrome | vscode |
| Midnight Aurora Ember | `#13110f` warm dark | sage / rose / amber | vscode |
| Midnight Aurora Tide | `#0b121a` blue-black | ice cyan / steel purple | vscode |

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
