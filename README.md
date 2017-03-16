# commands
Keeping track of useful Shell commands


### copy specific files inside folders keeping the directory hierarchy structure
```sh
rsync -av --include="*/" --include="*-pose.csv" --exclude="*" mo@air540:Desktop/HADComplianceGroundTruth1/ data/
```

### pretty log for git
```sh
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```
