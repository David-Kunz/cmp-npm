# cmp-npm

This is an additional source for [nvim-cmp](https://github.com/hrsh7th/nvim-cmp), it allows you to
autocomplete [npm](https://npmjs.com/) packages and its versions.
The source is only active if you're in a `package.json` file.

![demo-cmp-npm](https://user-images.githubusercontent.com/1009936/138598207-4855e5b5-1a88-4b02-b43a-c67143527f82.gif)

## Requirements

It needs the Neovim plugin [nvim-cmp](https://github.com/hrsh7th/nvim-cmp) and the [npm](https://npmjs.com/) command line tool.

## Installation

For [vim-plug](https://github.com/junegunn/vim-plug):
```
Plug 'nvim-lua/plenary.nvim'
Plug 'David-Kunz/cmp-npm'
```
For [packer](https://github.com/wbthomason/packer.nvim):
```
use {
  'David-Kunz/cmp-npm',
  requires = {
    'nvim-lua/plenary.nvim'
  }
}
```

Run the `setup` function and add the source
```lua
require('cmp-npm').setup({})
cmp.setup({
  ...,
  sources = {
    { name = 'npm', keyword_length = 4 },
    ...
  }
})
```
(in Vimscript, make sure to add `lua << EOF` before and `EOF` after the lua code)

## Configuration

Default config:
```lua
require('cmp-npm').setup({
  -- show only semantic versions (MAJOR.MINOR.PATCH)
  -- 'false' will show all available versions
  only_semantic_versions = false,
  -- if specified, will not show provided version labels
  -- works only if only_semantic_versions is set to false
  -- for example: { 'beta', 'rc', 'dev', 'insiders', 'experimental' }
  ignore = {},
})
```


## Limitations

The versions are not correctly sorted (depends on `nvim-cmp`'s sorting algorithm).
