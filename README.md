# 🚀 My Developer Setup

## 1. Terminal + Shell

- Windows Terminal
- PowerShell 7
- PSReadLine
  - Predictive IntelliSense
  - History Suggestions
  - ListView Completion Menu

---

## 2. Terminal UI / Prompt

- Starship
  - Modern shell prompt
  - Git integration
  - Language detection
  - Customizable modules

---

## 3. Command Line Productivity

- fzf
  - Fuzzy search
  - History search
  - Interactive filtering

- ripgrep (rg)
  - Fast content search

- fd
  - Fast file finder

- zoxide
  - Smarter `cd`
  - Frecency-based navigation

- eza
  - Better `ls`
  - Icons
  - Git status support
  - Tree view

---

## 4. Git Tools

- Git

- LazyGit
  - TUI Git manager
  - Commits
  - Branches
  - Rebases
  - Stashes
  - Diffs

> Integrated with Neovim but can also run independently from any terminal.

---

## 5. AI / Coding Assistants

- OpenCode CLI
- GitHub Copilot CLI

---

## 6. Compiler / Build Tools

### C / C++

- GCC
- G++

### Environment

- MSYS2 Toolchain

### Other Languages

- Python
- Node.js
- npm

---

### 7. Status bar and window manager

- Glazewm (Widow tiling manager)
- YASB (Status Bar)

---

## 8. Editor Ecosystem

### Neovim

#### Plugin Manager

- lazy.nvim

#### Dashboard

- alpha.nvim

#### UI

- bufferline.nvim
- lualine.nvim
- rose-pine
- dressing.nvim
- vim-maximizer

#### File Navigation

- nvim-tree.lua
- telescope.nvim

#### Syntax & Parsing

- nvim-treesitter
- nvim-treesitter-textobjects
- treesitter-playground

#### Completion & Snippets

- nvim-cmp
- cmp-nvim-lsp
- LuaSnip
- cmp_luasnip

#### Editing Experience

- nvim-autopairs

#### Development

- LSP
  - clangd
  - pyright
  - ts_ls

- conform.nvim
- code_runner.nvim

#### Git Integration

- gitsigns.nvim
- lazygit.nvim

#### Terminal Integration

- toggleterm.nvim

---

## Workflow

```text
Windows Terminal
    ↓
PowerShell + Starship
    ↓
Neovim
    ↓
OpenCode / Copilot
    ↓
GCC / Python / Node.js
    ↓
LazyGit
```

---

## Philosophy

- Terminal-first
- Keyboard-driven
- Fast startup
- Low resource usage
- Minimal distractions
- Build more, configure less
