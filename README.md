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

3. Check if base branch has ahead commits of subbranch

```
git rev-list --count branch1..basebranch
```

if return = 0, it means that there is no changes ahead
