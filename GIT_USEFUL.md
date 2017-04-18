### git useful commands

Pretty log for git:
```sh
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all"
```

Print list of tracked files by git:
```sh
git log --pretty=format: --name-only --diff-filter=A | sort - | sed '/^$/d'
```

Print list of tracked files by git (only existing): 
```sh
git ls-tree -r HEAD --name-only
```

Remove a file from all commits: 
```sh
git filter-branch -f --tree-filter 'rm -f file' HEAD
```
