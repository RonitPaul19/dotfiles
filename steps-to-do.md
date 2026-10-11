# Windows Development Environment Setup

Personal setup checklist for Windows 11, PowerShell 7, Neovim, and C/C++.

> Run commands in PowerShell 7 unless a section explicitly says to use MSYS2 UCRT64.

## 1. Install PowerShell 7

```powershell
winget install --id Microsoft.PowerShell --exact --source winget
```

## 2. Install Git

```powershell
winget install --id Git.Git --exact --source winget

git config --global user.name "name"
git config --global user.email "your-email@exaple.com"
```

Verify:

```powershell
git --version
git config --global --list
```

## 3. Install Neovim

```powershell
winget install --id Neovim.Neovim --exact --source winget
```

Clone my Neovim configuration:

```powershell
git clone https://github.com/RonitPaul19/nvim.git "$env:LOCALAPPDATA\nvim"
```

Verify:

```powershell
nvim --version
```

## 4. Install CLI Tools

```powershell
winget install --id Starship.Starship --exact --source winget
winget install --id junegunn.fzf --exact --source winget
winget install --id BurntSushi.ripgrep.MSVC --exact --source winget
winget install --id sharkdp.fd --exact --source winget
winget install --id ajeetdsouza.zoxide --exact --source winget
winget install --id eza-community.eza --exact --source winget
winget install --id marlocarlo.psmux --exact --source winget
```

Verify after opening a new terminal:

```powershell
starship --version
fzf --version
rg --version
fd --version
zoxide --version
eza --version
```

## 5. Install Node.js and npm

```powershell
winget install --id OpenJS.NodeJS.LTS --exact --source winget
```

Verify:

```powershell
node --version
npm --version
```

## 6. Install Python

```powershell
winget install --id Python.Python.3.14 --exact --source winget
```

Verify:

```powershell
python --version
python -m pip --version
```

## 7. Install OpenCode CLI

Install Node.js first.

```powershell
npm install --global opencode-ai
```

Verify:

```powershell
opencode --version
```

## 8. Install MSYS2 for C/C++

Install MSYS2 from PowerShell:

```powershell
winget install --id MSYS2.MSYS2 --exact --source winget
```

Open **MSYS2 UCRT64** from the Windows Start menu.

### Update MSYS2

Run inside the UCRT64 terminal:

```bash
pacman -Syu
```

If prompted to close the terminal, close it, reopen UCRT64, and run the update again until complete.

### Install GCC, G++, and build tools

Run inside UCRT64:

```bash
pacman -S --needed base-devel mingw-w64-ucrt-x86_64-toolchain
```

Verify inside UCRT64:

```bash
gcc --version
g++ --version
gdb --version
which gcc
which g++
```

### Add UCRT64 to Windows PATH

Add this directory to your Windows user PATH:

```text
C:\msys64\ucrt64\bin
```

Do not add `C:\msys64\usr\bin` to the Windows PATH.

Open a new PowerShell terminal and verify:

```powershell
gcc --version
g++ --version
gdb --version
```

> GCC/G++ installation does not automatically install Clang or `clangd`. Install them separately if needed by your Neovim configuration.

## 9. Install a Nerd Font

Install a Nerd Font if your terminal or Neovim configuration uses icons. Select it in your terminal's font settings.

## 10. Final Verification

Open a new PowerShell 7 terminal:

```powershell
pwsh --version
git --version
nvim --version
node --version
npm --version
python --version
gcc --version
g++ --version
gdb --version
opencode --version
```

If a command is not recognized, open a new terminal first. If it still fails, check the installation and PATH.

## Notes

- Use Winget for Windows applications and `pacman` inside MSYS2 UCRT64 for MSYS2 packages.
- Keep the Neovim configuration at `%LOCALAPPDATA%\nvim`.
- Install only the additional language servers, formatters, and Treesitter parsers your Neovim configuration needs.
- If Winget cannot find a package ID, search for the current package ID before changing the command.
