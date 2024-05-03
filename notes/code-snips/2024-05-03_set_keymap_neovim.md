---
date: 2024-05-03
tags:
    - code-snip
hubs:
    - "[[vim]]"
---
#  Set Keymap Neovim

Need to remember how to set up my keymaps in Neovim

```lua

local opts = { noremap = true, silent = true }
local term_opts = { silent = true }

-- shorten function name
local keymap = vim.api.nvim_set_keymap

-- remap space as leader key
vim.g.mapleader = " "
vim.g.maplocalleader = " "

-- save file
keymap("n", "<leader>w", "<Cmd>w<CR>", opts)
-- quit neovim
keymap("n", "<leader>q", "<Cmd>q<CR>", opts)
```

