# Agent conventions

This repo holds editor themes. Palettes are shared. Ports are editor-native files.

## Where to work

- Change colors in `palettes/<theme>.json` first.
- Then update every port that already exists for that theme.
- Put editor files only under `ports/<editor>/`.

## Do not

- Hard-code a new hex in a port when the same role already exists in the palette.
- Duplicate the VS Code theme into `ports/cursor` or `ports/antigravity-ide`. Those editors load `ports/vscode`.
- Add a build step, npm workspace, or generated theme pipeline unless asked.

## VS Code family

Antigravity IDE and Cursor use the VS Code color-theme contribution (`package.json` `contributes.themes`, `uiTheme`, TextMate `tokenColors`, workbench `colors`). Keep that port valid as a local extension: a folder with `package.json` plus the theme JSON.

Dark variants of Midnight Aurora live next to the Subtle theme and use the official `"include"` field to inherit token rules, then override `colors` / semantic tokens. Do not copy the full Subtle JSON for a new dark background — add a palette and an include file.
