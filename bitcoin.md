## Squash several commits into a single one and rebase on master

```
git checkout master
git pull
git checkout feature/branch
git reset HEAD~
git stash
git rebase master
git stash pop
# resolve merge
git add ...
git commit
git push --force
```
However, squashing commits for a nice history is a bad idea because you can't do binary search anymore. Small commits have value.

## Add changes to the last commit (can save the squashing)
```
git add ...
git commit --amend
```

## Compare two branches just by filenames
```
git diff --name-status master..feature/username/ticketnumber
```

## Show changed/added files of last 2 commits
```
git log -n 2 --name-status
```

## Show local branches sorted by date with date ascending
```
git for-each-ref --sort=committerdate refs/heads/ --format='\''%(committerdate:short) %(refname:short)'\'''
```
