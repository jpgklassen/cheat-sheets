## Branches

### List all branches

`git branch` to list local branches, `git branch -r` to list remote branches

### Switch branches
`git checkout <branch-name>`

### Moving existing edits to a new branch
`git switch -c <new-branch>`

### Rename the current branch (no remote)

`git branch -m <new-name>`

## Stash

### Add to stash
`git stash push -m "<stash-name>"`

### List stashes
`git stash list`

### Popping the stash
`git stash pop` pops the top stash  
`git stash pop stash@{n}` pops the nth stash  
`git stash pop stash^{/stash-name}` pops the stash named stash-name

Resolving stash conflicts without a commit:
```
$ git stash pop
## ...resolve conflict(s)
$ git restore --staged .
$ git stash drop
```

## Undoing

### Undoing an add
`git reset <file>` to reset one file, `git reset` to reset all files.

### Undoing a commit
`git reset HEAD~`

### Undoing a push
`git push -f origin last_known_good_commit:branch_name`

## Settings

### List current settings
`git config --list --show-origin`

### Update setting
`git config [--global] setting.name <value>`

### Delete setting
`git config [--global] --unset setting.name`