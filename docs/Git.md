- https://github.com/git-tips/tips

## Git commit header
- **feat**: introduce a new feature
- **fix**: patches a bug in your codebase (bugfix or hotfix)
- **build**: changes that affect the build system or external dependencies
- **chore**: updates dependencies and does not relate to fix or feat and does not modify src or test files.
- **ci**: changes that affect the continuous integration process
- **docs**: updates the documentation or introduce documentation
- **style**: updates the formatting of code; remove white spaces, add missing spaces, remove unnecessary newlines
- **refactor**: reactors code segments to optimize readability without changing behavior
- **perf**: improve performance
- **test**: add/remove/update tests
- **revert**: reverts one or many previous commits

## Cache your login credentials in Git

```git
git config --global credential helper store
```

## Fix error with renamed repo

```git
git remote set-url origin <url>
```
Or
```git
git remote rm origin
git remote add origin <url>
```

## Fix git error: failed to push some refs to remote

```git
git pull --rebase origin main
git push origin main
```

## Clone large git project (shallow clone)

```
git clone --depth <depth> -b <branch> <repo_url>
```


## Git alias

Copy this to the `.gitconfig` file

```git
[alias]
	p = push
	cm = commit
	br = branch
	st = status
	co = checkout
	last = log -1 HEAD
	lg = log --pretty=format:\"%Cgreen%h %Creset%cd %Cblue[%cn] %Creset%s%C(yellow)%d%C(reset)\" --graph --date=relative --decorate
```

## Git options

```git
git diff --word-diff
```
![](https://blog.gitbutler.com/content/images/size/w1000/2024/02/CleanShot-2024-02-08-at-08.19.28@2x.png)

## Apply commit from other branch to current branch

```git
git cherry-pick <commit>
```

Be sure to switch branch before cherry picking


## Git stash commands
```git
git stash
git stash save (deprecated) -> git stash push -m "<message>"
git stash list
git stash show, git stash show -p
git stash pop  		remove stashed state from the stash list and apply it
git stash apply		like `pop`, but do not remove the state from the stash list
git stash drop 		delete a single stash entry
git stash clear 	delete all stash
```

## Pull submodule
```git
git submodule foreach git pull
```