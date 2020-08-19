# git-tips

1. reset local branch to it's origin version
```
git fetch origin
git reset --hard origin/master
```

2. reset file version to branch version

```
git checkout {branchname} -- {path-to-file}
```
