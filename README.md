# Cheat Sheet
Keeping track of useful Shell commands


### copy specific files inside folders keeping the directory hierarchy structure
```sh
rsync -av --include="*/" --include="*-pose.csv" --exclude="*" mo@air540:Desktop/HADComplianceGroundTruth1/ data/
```

### pretty log for git
```sh
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```
### git useful commands

- Print list of tracked files by git:

```sh
git log --pretty=format: --name-only --diff-filter=A | sort - | sed '/^$/d'
```

- Print list of tracked files by git (only existing): 

```sh
git ls-tree -r HEAD --name-only
```

- Remove a file from all commits: 

```sh
git filter-branch -f --tree-filter 'rm -f file' HEAD
```
### git merge with submodule

```sh
# Fetch the submodule commits into the main repository
git remote add submodule_origin git://url/to/submodule/origin
git fetch submodule_origin

# Start a fake merge (won't change any files, won't commit anything)
git merge -s ours --no-commit submodule_origin/master

# Do the same as in the first solution
git rm --cached submodule_path # delete reference to submodule HEAD
git rm .gitmodules             # if you have more than one submodules,
                               # you need to edit this file instead of deleting!
rm -rf submodule_path/.git     # make sure you have backup!!
git add submodule_path         # will add files instead of commit reference

# Commit and cleanup
git commit -m "removed submodule"
git remote rm submodule_origin
```
