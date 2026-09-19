# Midnight Aurora Subtle — VS Code

VS Code color theme for this palette. Antigravity IDE and Cursor load this same port.

## Install (local extension)

From this folder, or from the repo root using the vscode port path:

**VS Code**

```sh
ln -sfn "$HOME/Workspace/Repos/my-editor-themes/ports/vscode" \
  "$HOME/.vscode/extensions/kanthi.midnight-aurora-subtle"
```

Reload the window, then set Color Theme to **Midnight Aurora Subtle**.

To package a VSIX later:

```sh
npx @vscode/vsce package
```

## Format

Follows the VS Code color theme contribution:

- `package.json` → `contributes.themes`
- `uiTheme`: `vs-dark`
- workbench `colors`
- TextMate `tokenColors`
- `semanticHighlighting` + `semanticTokenColors`

## Language scopes

Generic tokens plus grammar-specific rules for:

- **Frontend:** JavaScript, JSX, TypeScript, TSX, HTML, CSS, SCSS, Less, JSON, GraphQL, YAML, TOML
- **Backend:** Go, Rust, Python
- **Also:** Shell

Scopes match the grammars bundled in VS Code / Antigravity IDE (`source.go`, `source.rust`, MagicPython, JS/TS/TSX, HTML, CSS). Semantic tokens cover rust-analyzer, gopls, and Pylance (`lifetime`, `macro`, `builtinType`, `decorator`, `selfKeyword`).
