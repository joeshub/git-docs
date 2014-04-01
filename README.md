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
#### add - create a submodule in your project from a master branch
```shell
git submodule add -b master git@hostname:project.git path/to/where/it/should/go
git submodule init
git submodule update
git add .
git commit -a -m "message"
git push --recurse-submodules=on-demand
```
this will create a .gitmodules file in your project that looks like this:
```config
[submodule "path/to/where/it/should/go"]
	path = path/to/where/it/should/go
	url = git@hostname:project.git
	branch = master
```

#### update - pull down submodules in a cloned project
```shell
git submodule update --init
```

#### update - get updates to changes in submodules from branch used in -b
```shell
git submodule update --remote
```
to avoid fetching files use:
```shell
git submodule update --remote --no-fetch 
```

#### status - find changes in submodules, + shows additions
```shell
git submodule status
```

#### remove - remove a submodule from your project
```shell
git submodule deinit submodulename    
git rm submodulename
optionally to leave the files in your working tree
git rm --cached submodulename
```
