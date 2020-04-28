# git-cheatsheet
> Git features that have proven to be very useful for developers

## Configurations

`# set the global username`

```bash
git config --global user.name "John Doe"
```

`# set the global user email`

```bash
git config --global user.mail "johndoe@domain.com"
```

`# set the local username`

```bash
git config --local user.name "John Doe"
```

`# set the local user email`

```bash
git config --local user.mail "johndoe@domain.com"
```

`# to unset a given configuration`

```bash
git config --global --unset-all user.name

```

`# to list global configurations`

```bash
git config --global --list
```

`# to replace configurations`

```bash
git config --global --replace-all user.name "New User Name"
```

`# to ignore file mode changes (i.e file permissions)`

```bash
git config core.fileMode false
```

`# to ignore new line character differences between systems (windows-linux)`

```bash
git config --global core.autocrlf true
```

## Working with remotes

`# list all the configured remote repositories`

```bash
git remote
```

`# remove a remote address for the repository`

```bash
git remote rm <remote>
```

`# change url if specific remote (<origin>, <upstream>, etc.)`

```bash
git remote set-url origin https://github.com/username/repo.git
```

`# to push all your branches.`

```bash
git push <remote> --all
```

`# to push all your tags`

```bash
git push <remote> --tags
```

`# prunes tracking branches not on the remote`

```bash
git remote prune origin
```

## Working with Branches

`# list all the branches`

```bash
git branch
```

`# list all the branches (local and repote branches)`

```bash
git branch --all
```

`# make a switch to a specified branch`

```bash
git checkout <branch>
```

`# deleting specified branch`

```bash
git branch -d <branch>
```

`# tracking a remote branch`

```bash
git branch -u <remote>/<branch>
```

`# to remove all branches locally that have been already removed from origin`

```bash
git remote prune origin
```

`# sorting branches by date of last commit`

```bash
git branch --sort=-committerdate  # DESC
git branch --sort=committerdate  # ASC
```

```bash
git for-each-ref --sort=committerdate refs/heads/ --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'
```

## Stashing

`# stash/save local changes`

```bash
git stash save "updated the offline file"
```

`# apply stashed changes (at the top of stack) to working dir`

```bash
git stash pop
```

`# list stashed changes on the stack`

```bash
git stash list
```

## Reverting to previous states

### Reverting Files

`# showing file snapshot at specific commit`

```bash
git show <commit-sha>:relative/path/to/file/inside/repo
```

`# saving file snapshot at specific commit`

```bash
git show <commit-sha>:relative/path/to/file/inside/repo > /new/path/to/file/content/at/selected/commit
```

## Graph history visualization

`# showing last commit`

```bash
git log -1 
```

`# showing the current local history (-5 last five commits)`

```bash
git log --decorate --graph -5
```

`# showing commits after a specific date`

```bash
git log --date=local --after="2014-02-12T16:36:00-07:00"
```

## External links

* https://csswizardry.com/2017/05/little-things-i-like-to-do-with-git/
