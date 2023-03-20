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
set tabstop=8             
set softtabstop=0          
set shiftwidth=4        
set smarttab            
set expandtab  
```