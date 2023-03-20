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

## Fix error with renamed repo on Github

```git
git remote set-url origin [updated link url]
```
Or 
```git
git remote rm origin
git remote add origin [updated link url]
```

## Fix git error: failed to push some refs to remote

```git
git pull --rebase origin main
git push origin main
```

### Clone large git project

```
git clone --depth <depth> -b <branch> <repo_url>
```
