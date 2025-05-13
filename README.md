# gen-vimdoc.nvim

Generate vimdoc help files from lua/c docstrings, ported from
[neovim's `gen_vimdoc.lua` script](https://github.com/neovim/neovim/blob/master/src/gen/gen_vimdoc.lua).

## Usage

```lua
require('gen').run({
  target_1 = {
    filename = ..., -- path to doc
    files = {
      ..., -- source files
    },
    section_order = {
      ..., -- order or source files
    },
    section_fmt = function(name)
      return name
    end,
    helptag_fmt = function(name)
      return name:lower()
    end,
  },
})
```

## Examples

Plugin [dropbar.nvim](https://github.com/Bekaboo/dropbar.nvim) use this project
to [generate vimdoc from lua docstrings](https://github.com/Bekaboo/dropbar.nvim/blob/master/scripts/gen_vimdoc_from_src.lua).
