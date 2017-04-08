# Cheat Sheet
Keeping track of useful Shell commands


### filter copied files keeping the directory structure intact
```sh
rsync -av --include="*/" --include="*-pose.csv" --exclude="*" <source> <destination>
```
