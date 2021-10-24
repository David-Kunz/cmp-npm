# cmp-npm

This is an additional source for [nvim-cmp](https://github.com/hrsh7th/nvim-cmp), it allows you to
autocomplete [npm](https://npmjs.com/) packages and its versions.
The source is only active if you're in a `package.json` file.

![demo-cmp-npm](https://user-images.githubusercontent.com/1009936/138598207-4855e5b5-1a88-4b02-b43a-c67143527f82.gif)

## Requirements

It needs the `npm` command line tool.

## Installation

For [vim-plug](https://github.com/junegunn/vim-plug):
```
Plug 'nvim-lua/plenary.nvim'
Plug 'David-Kunz/cmp-npm'
```
For [packer](https://github.com/wbthomason/packer.nvim):
```
use 'nvim-lua/plenary.nvim'
use 'David-Kunz/cmp-npm'
```

## Limitations

The versions are not correctly sorted (depends on `nvim-cmp`'s sort algorithm).
