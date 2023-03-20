#### Copt this to the `.gitconfig` file

```git
[alias]
	p = push
	cm = commit
	br = branch
	st = status
	co = checkout
	last = log -1 HEAD
	lg = log --pretty=format:\"%Cgreen%h %Creset%cd %Cblue[%cn] %Creset%s%C(yellow)%d%C(reset)\" --graph --date=relative --decorate --all
```