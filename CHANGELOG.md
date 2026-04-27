# Changelog

All notable changes to `rbr.vscode` are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.0] — 2026-04-22

### Added
- Initial RBR (Classic flavor) theme based on [Amdhj22/rbr](https://github.com/Amdhj22/rbr) palette `v2.1.0`.
- Workbench colors covering activity bar, side bar, tabs, status bar, panels, terminal, peek view, merge editor, diff editor, notifications, menus, and quick picks.
- TextMate `tokenColors` for keywords, strings, numbers, functions, types, variables, decorators, tags, markdown, JSON/YAML/CSS specifics, and diff markup.
- Semantic `semanticTokenColors` mapping aligned with [Amdhj22/rbr.nvim](https://github.com/Amdhj22/rbr.nvim) so the same buffer renders consistently across Neovim and VS Code.
- Terminal ANSI 0–15 follow the canonical RBR ANSI mapping in `STYLE-GUIDE.md`.
