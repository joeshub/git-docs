git-docs
========

### conflicts
#### find all conflicted files:
```shell
git diff --name-only --diff-filter=U
```

### merging
#### revert an active merge
```shell
git merge --abort
```

### stash
#### add - save your work in progress
```shell
git stash
```

#### list - show all stashed work
```shell
git stash list
```

#### apply - bring back the last stash, or one one by name
```shell
git stash apply
git stash pop
git stash apply stash@{1}
```

#### drop - clear all stashes or drop a stash by name
```shell
git stash clear
git stash drop stash@{1}
```

### submodules
#### add - create submodules in your project
```shell
git submodule add git@hostname:project.git path/to/where/it/should/go
git submodule init
git submodule update
git add .
git commit -a -m "message"
git push --recurse-submodules=on-demand
```

#### update - pull down submodules in a project
```shell
git submodule init
git submodule update
or git submodule update --init
```

#### remove - remove a submodule from your project
```shell
git submodule deinit submodulename    
git rm submodulename
optionally to leave the files in your working tree
git rm --cached submodulename
```
