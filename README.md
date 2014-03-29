git-docs
========

## conflicts
### find all conflicted files:
git diff --name-only --diff-filter=U

## merging
### revert an active merge
git merge --abort

## stash
### add - save your work in progress
git stash

### list - show all stashed work
git stash list

### apply - bring back the last stash, or one one by name
git stash apply
git stash pop
git stash apply stash@{1}

### drop - clear all stashes or drop a stash by name
git stash clear
git stash drop stash@{1}
