## Vim moves
### Normal mode
- `Ctrl + w + v` or `:vp`: Split new buffer vertically
- `Ctrl + w + s` or `:sp`: Split new buffer horizontally
- `Ctrl + w + o`: Close all buffer except the current buffer
- `H`: Move to top of screen
- `M`: Move to middle of screen
- `L`: Move to bottom of screen
- `zz`: Center the current line on screen
- `viw`/`yiw`: Select/Yank a word, no matter where the cursor position on
- `gt`, `gT`: Ctrl Tab, Ctrl Shift Tab in Vim
- `~`: Change upper case to lower case and vice versa

### Visual mode
- `o`, `O`: Make the cursor go to the other end, useful for quickly changing the size of the selected text.


## Jump to the matching bracket/brace 
- Use `%` when your cursor on a bracket/brace

## Indent/Unindent a line or multiple lines
```
>> ⁠– indents a line
<< ⁠– unindents a line
> ⁠– indents multiple lines
< ⁠– unindents multiple lines
```

## For tab characters that appear 4-spaces-wide:
Put this in vimrc
```vim
set tabstop=4
set softtabstop=4
set shiftwidth=4
set smarttab
set expandtab
```