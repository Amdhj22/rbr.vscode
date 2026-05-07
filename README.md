<h1 align="center">
  🏁&nbsp;&nbsp;rbr.vscode
</h1>

<p align="center">
  <i>A Red Bull Racing colorscheme for Visual Studio Code — the VS Code port of <a href="https://github.com/Amdhj22/rbr">rbr-theme</a>.</i>
</p>

<p align="center">
  <a href="https://github.com/Amdhj22/rbr.vscode/stargazers"><img src="https://img.shields.io/github/stars/Amdhj22/rbr.vscode?colorA=0a1128&colorB=e84a55&style=for-the-badge"/></a>
  <a href="./LICENSE"><img src="https://img.shields.io/github/license/Amdhj22/rbr.vscode?colorA=0a1128&colorB=b8d49e&style=for-the-badge"/></a>
  <a href="https://github.com/Amdhj22/rbr"><img src="https://img.shields.io/badge/palette-rbr--theme-e84a55?colorA=0a1128&style=for-the-badge"/></a>
</p>

&nbsp;

## About

`rbr.vscode` paints VS Code with the [RBR color scheme](https://github.com/Amdhj22/rbr) — a **three-accent** palette: **kerb red** for what's active, **RB yellow** for what needs attention, **chequer white** for functions / methods. A deep navy base keeps the trio readable. See the upstream [`STYLE-GUIDE.md`](https://github.com/Amdhj22/rbr/blob/main/STYLE-GUIDE.md) for the full design rules.

> [!NOTE]
> This scheme is a fan tribute. Not affiliated with or endorsed by Red Bull Racing, Oracle Red Bull Racing, or Red Bull GmbH.

&nbsp;

## Install

### From a `.vsix` release (current)

1. Download the latest `rbr-*.vsix` from the [Releases](https://github.com/Amdhj22/rbr.vscode/releases) page.
2. Install:
   ```bash
   code --install-extension rbr-0.1.0.vsix
   ```
3. `Cmd+K Cmd+T` (macOS) or `Ctrl+K Ctrl+T` → pick **RBR**.

### From source

```bash
git clone https://github.com/Amdhj22/rbr.vscode.git
cd rbr.vscode
npx @vscode/vsce package
code --install-extension rbr-0.1.0.vsix
```

### From the VS Code Marketplace

Coming soon. Once published, install via the Extensions tab (`Ctrl+Shift+X`) → search **RBR**.

&nbsp;

## What it paints

`rbr.vscode` covers all three highlighting layers VS Code exposes:

| Layer | What it covers |
|---|---|
| **Workbench colors** (≈ 200 keys) | Activity bar, side bar, tabs, status bar, terminal, git decorations, peek view, merge editor, notifications, menus, quick picks |
| **TextMate scopes** (`tokenColors`) | Per-language syntax highlighting via TextMate grammar scopes — works in any language with a grammar (most of them) |
| **Semantic tokens** (`semanticTokenColors`) | LSP-driven token coloring (Neovim 0.9+ equivalent) — overrides TextMate when an LSP is attached |

Highlights of the painting choices:

- **Active editor tab top border** = Kerb Red — only one tab is "the one"
- **Cursor** = RB Yellow — the always-attention pixel
- **Selected line / matching bracket border** = Kerb Red
- **Find match** = RB Yellow border + soft fill
- **Activity bar active item border** = Kerb Red
- **Status bar debugging mode** = Kerb Red bg ("you're debugging now")
- **Git decorations**: added → Paddock Green, modified → RB Yellow, deleted → Kerb Bright, renamed → Sky Blue, conflict → Kerb Red
- **Terminal ANSI 16** = full RBR mapping (matches `Amdhj22/rbr` palette)

&nbsp;

## Companion ports

For a consistent look across the rest of your stack:

| Tool | Repo |
|---|---|
| Neovim | [Amdhj22/rbr.nvim](https://github.com/Amdhj22/rbr.nvim) |
| Obsidian | [Amdhj22/rbr.obsidian](https://github.com/Amdhj22/rbr.obsidian) |
| tmux | [Amdhj22/rbr.tmux](https://github.com/Amdhj22/rbr.tmux) |
| Ghostty / iTerm2 / Powerlevel10k / eza | [Amdhj22/rbr](https://github.com/Amdhj22/rbr) |

&nbsp;

## Development

```bash
git clone https://github.com/Amdhj22/rbr.vscode.git
cd rbr.vscode
code .
# Press F5 to launch an Extension Development Host with the theme loaded.
# In that window: Cmd+K Cmd+T → RBR
```

Editing `themes/rbr-color-theme.json` updates the host window live (no reload needed for most keys).

To produce a `.vsix`:

```bash
npx @vscode/vsce package
```

To publish to the Marketplace (requires a [publisher account](https://marketplace.visualstudio.com/manage) and an Azure DevOps PAT):

```bash
npx @vscode/vsce publish
```

&nbsp;

## License

[MIT](./LICENSE) © Amdhj22
