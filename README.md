<p align="center">
  <img src="banner.png" alt=".dotfiles" width="750" height="150">
</p>

Repo containing my configuration files. For easily stowing of configs clone the
repo in `$HOME`.

![Opening a NestJS project file using nnn and nvim](https://i.imgur.com/WKd4tVB.gif)

# Contents

1. [Getting Started](#Getting_Started)
    1. [Neovim](#Neovim)
        1. [General](#General)
        2. [Intellisense](#Intellisense)
2. [Usage](#Usage)

# Getting Started

Below are the prerequisites and setup per (config) folder where necessary.
To make sure you have all dependencies needed you could have a look at
`pklist.txt` which programs are installed an sensibly pick those you would need
for a directoty/program setup.

>💡 On Arch, pereferably install packages and language servers using _pacman_ instead of
'npm-installing', using scripts, etc.

## Neovim

After stowing `nvim` (see [Usage](#Usage)), installing the LSP servers below
and running `:PlugInstall` in neovim, supported languages & files should be:
  - Vim configuration files
  - Dockerfiles
  - Ansible (y[a]ml files)
  - LaTeX
  - JavaScript
  - TypeScript
  - Python
  - Lua
  - Rust
  - java

### General

[Vim plug](https://github.com/junegunn/vim-plug) is used for plugin management
-- make sure to install it.  For python support install
[pynvim](https://github.com/neovim/pynvim) and set the global python
environment (/usr/bin/python).

### Intellisense

For intellisense to work, install the following language servers that implement
the LSP protocol:
  - [vimls](https://github.com/iamcco/vim-language-server)
  - [dockerls](https://github.com/rcjsuen/dockerfile-language-server-nodejs)
  - [Ansible language server](https://github.com/ansible/ansible-language-server)
  - [texlab](https://github.com/latex-lsp/texlab)
    >❗TexLab only implements the LSP; to be able to build `.tex` files install
    _Tectonic_ and _biber_ to be able to create references and citations.
  - [tsserver](https://github.com/typescript-language-server/typescript-language-server)
  - [pyright](https://github.com/microsoft/pyright)
  - [sumneko/lua-language-server](https//github.com/sumneko/lua-language-server)
  - [rust-analyzer](https://github.com/rust-analyzer/rust-analyzer)
  - For java [CoC](https://github.com/neoclide/coc.nvim) is used since native
    LSP didn't work with debugging.

# Usage

Stow is used to create symlinks, just run `stow <directory>` from within the
repo directory, e.g. `stow nvim`.  This will stow the `nvim` directory one
directory up from where the repo is cloned.

>💡 For ease of use, clone the repo from within your home folder, resulting in
`$HOME/.dotfiles`. This ensures that symlinks to a (config file in) `<folder>`
are in the locate where the program is expecting it's config files.

In my case, I cloned the repo into `$HOME/.dotfiles`. Running the above command
will result in `$HOME/.config/nvim -> $HOME/.dotfiles/nvim/.config/nvim` (a
symlink in the `.config` folder -- nvim -- pointing to the `nvim` folder in the
dotfiles repo).

