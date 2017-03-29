# linux_config
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
git ls-tree -r master --name-only
```

- Remove a file from all commits: 

```sh
git filter-branch -f --tree-filter 'rm -f file' HEAD
```

