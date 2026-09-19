# Midnight Aurora Subtle — VS Code

VS Code color theme for this palette. Antigravity IDE and Cursor load this same port.

## Install (local extension)

From this folder, or from the repo root using the vscode port path:

**VS Code**

```sh
ln -sfn "$HOME/Workspace/Repos/my-editor-themes/ports/vscode" \
  "$HOME/.vscode/extensions/kanthi.midnight-aurora-subtle"
```

Reload the window, then set Color Theme to one of:

- **Midnight Aurora Subtle** — original navy (`#0e1319`)
- **Midnight Aurora Void** — darker near-black
- **Midnight Aurora Dusk** — lifted navy
- **Midnight Aurora Ember** — warm dark
- **Midnight Aurora Tide** — cool blue-black
- **Midnight Aurora Haze** — warm stone, lowest contrast

Variants use VS Code's theme `include` of the Subtle file, then override workbench `colors`, semantic tokens, and the full TextMate token set so language-specific scopes follow that variant's palette.

To package a VSIX later:

```sh
npx @vscode/vsce package
```

## Format

Follows the VS Code color theme contribution:

- `package.json` → `contributes.themes`
- `uiTheme`: `vs-dark`
- workbench `colors` (including chat, inline chat, sticky scroll, and inlay hints)
- TextMate `tokenColors`
- `semanticHighlighting` + `semanticTokenColors`

## Language scopes

Generic tokens plus grammar-specific rules for:

- **Frontend:** JavaScript, JSX, TypeScript, TSX, HTML, CSS, SCSS, Less, JSON, GraphQL, YAML, TOML
  - HTML: tags, attributes, values, entities, doctype
  - CSS: selectors, properties, units (`px`/`em`/…), at-rules, custom properties, SCSS `$variables`
- **Backend:** Go, Rust, Python
- **Also:** Shell

Scopes match the grammars bundled in VS Code / Antigravity IDE (`source.go`, `source.rust`, MagicPython, JS/TS/TSX, HTML, CSS). Semantic tokens cover rust-analyzer, gopls, and Pylance (`lifetime`, `macro`, `builtinType`, `decorator`, `selfKeyword`).
