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

## Changing the Last Commit
```git
git commit --amend
```

## Restore modified file 
```git
git restore <file>
```

## Remove file from staging area
```git
git reset <file>
```

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

### Git stash specific file
```git
git stash push -m "<message>" <path>
```

## Pull submodule
```git
git submodule foreach git pull
```

## remove folder/directory from remote git repository

```git
git rm -r --cached <file/folder>
git commit -m "Removed <file/folder> from repository"
git push
```

### Remove file from remote git repository
```git
git rm --cached <file>
git commit -m "Stop tracking <file>"
git push
```

## Removing multiple files from a Git repo that have already been deleted from disk

```git
git add -u
```

## Add all files except a single file
```git
git add .
git reset -- main/file
git reset -- main/folder/*
```
or using pathspec magic `:(exclude)` and its short form `:!`
```git
git add . :!file :!folder/*
```

## Git tag
```git
git tag -a v1.0.0
git tag -a v1.0.0 -m "Releasing version v1.0.0"
git tag					listing tag
git push --tags
git checkout v1.0.0   	check out tag
git tag -d v1.0			delete tag
```

## Rename a file:
```git
git mv <old-name> <new-name>
```

## Ignore all change of commited and pushed file
Use this to tell Git to assume that a file has not changed, even if it has
```git
git update-index --assume-unchanged <file>
```
and undo it (want to resume tracking change again) using:
```
git update-index --no-assume-unchanged <file>
```

To get a list of dir's/files that are assume-unchanged run this in a unix shell:
```git
git ls-files -v | grep '^h'
```

or in a PowerShell:
```git
git ls-files -v | Select-String -CaseSensitive '^h'
```

But using `--assume-unchanged` still not enough when working with branches, so use `--skip-worktree` instead if you want to ignore local changes across branches
```git
git update-index --skip-worktree <file>
```
and check it:
```git
git ls-files -v | Select-String -CaseSensitive '^S'
```

Also, `--assume-unchanged` often used as a performance optimization: For large files that never actually change, this will skip checking these files.


Source: https://stackoverflow.com/a/17195901/16461323

But also note that in the official doc of `git update-index`:
> Users often try to use the assume-unchanged and skip-worktree bits to tell Git to ignore changes to files that are tracked. This does not work as expected, since Git may still check working tree files against the index when performing certain operations. **In general, Git does not provide a way to ignore changes to tracked files, so alternate solutions are recommended.**
> 
> For example, if the file you want to change is some sort of config file, the repository can include a sample config file that can then be copied into the ignored name and modified. The repository can even include a script to treat the sample file as a template, modifying and copying it automatically.
>
> https://git-scm.com/docs/git-update-index#_notes

