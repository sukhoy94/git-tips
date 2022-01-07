https://marklodato.github.io/visual-git-guide/index-pl.html?no-svg

# git-tips

1. reset local branch to it's origin version
```
git fetch origin
git reset --hard origin/master
```

2. reset file version to repository version

```
git checkout {branchname} -- {path-to-file}
```

3. Check if base branch has ahead commits of subbranch

```
git rev-list --count branch1..basebranch
```

if return = 0, it means that there is no changes ahead


4. Delete branch (locally and remote): 

```
git push -d <remote_name> <branch_name>
git branch -d <branch_name>
```

5. Cherry pick

Make sure you are on the branch you want to apply the commit to.
```
git checkout master
```

Execute the following:
```
git cherry-pick <commit-hash>
```

6. Create subbranch from branch

```
git checkout -b myFeature baseBranch
```

7. Add alias for command: 

```
git config --global alias.st status
```

8. Get list of aliases: 

```
git config --get-regexp alias
```

9. cherry-pick but change commit message: 

```
git cherry-pick -e <hash>
```

10. Add remote to local repo: 

```
git remote add origin git@github.com:User/UserRepo.git
git push -u origin master
```

11. Change remote origin

```
git remote remove origin
git remote add origin ORIGIN_URL
```

12. My git aliases list:

```
git config --global alias.st status
git config --global alias.cmt commit
git config --global alias.p push
git config --global alias.a add
git config --global alias.co checkout
git config --global alias.pl pull
```

## 3 important rules to work with GIT in team: 
```
1. Resolve conflicts only when you understand why they have arisen.
2. Always check the list of commits you push
3. Notified all developers if you have done push force.
```


