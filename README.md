# play

## Subtrees

### Adding a subtree

```git subtree add --prefix {local directory being pulled into} {remote repo URL} {remote branch} --squash```

For example:
```git subtree add --prefix subtreeDirectory git@github.com:smilee/subtreeDirectory.git main --squash```
will clone git@github.com:smilee/subtreeDirectory.git into the 'subtreeDirectory' directory.

### Adding the subtree as a remote

```git remote add -f subtreeDirectory git@github.com:smilee/subtreeDirectory.git```

### Fetch new subtree commits

```
git fetch subtreeDirectory main
git subtree pull --prefix subtreeDirectory subtreeDirectory main --squash
```