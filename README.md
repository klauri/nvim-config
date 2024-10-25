 # Bootstrap lazy.nvim

This repository contains a customized configuration for Neovim using the `lazy.nvim` plugin manager. The following is a brief overview of the setup and its components. For detailed information, please refer to the respective repositories linked below.

## Requirements

- Neovim (tested with version 0.8.1)

## Installation

To get started, make sure that you have the necessary dependencies installed. Then clone this repository and set up your `mapleader` and `maplocalleader` variables before loading `lazy.nvim`.

```bash
git clone https://github.com/yourusername/neovim-config.git --depth=1
cd neovim-config
mkdir -p ~/.local/share/lazy/lazy.nvim
ln -s $PWD/init.vim ~/.local/share/lazy/lazy.nvim/init.vim
```

Now, set your `mapleader` and `maplocalleader` variables:

```lua
vim.g.mapleader = " "
vim.g.maplocalleader = "\\"
```

## Plugins

The following plugins are included in this configuration:

1. [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim) (0.1.5 tag) with dependencies: [plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
2. [tokyonight.nvim](https://github.com/folke/tokyonight.nvim) (named "tokyonight")
3. [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter) with build command: `TSUpdate`
4. [harpoon](https://github.com/ThePrimeagen/harpoon) (branch "harpoon2") with dependencies: [plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
5. [vim-fugitive](https://github.com/tpope/vim-fugitive)
6. [lsp-zero.nvim](https://github.com/VonHeikemen/lsp-zero.nvim) (branch "v3.x") with dependencies: [mason.nvim](https://github.com/williamboman/mason.nvim), [mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim), [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig), [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp), [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp), [onsails/lspkind.nvim](https://github.com/onsails/lspkind.nvim)
7. [ollama](https://github.com/dandavison/ollama) (for AI model integration, see the [ollama](#ollama-configuration) section below)
8. Other settings and configurations are installed as needed.

## Ollama Configuration

To use the AI model integration provided by the `ollama` plugin, make sure that you have it installed and runnning (see the [ollama](https://github.com/ollama/ollama) repository for installation instructions). You may need to modify the configuration in this repository to suit your needs.

## Updating Plugins

To ensure that your plugins are always up-to-date, enable the `checker` module in your `lazy.nvim` configuration:

```lua
-- Configure any other settings here. See the documentation for more details.
-- automatically check for plugin updates
checker = { enabled = true },
```
