### Useful commands for Shell, Bash, ...

Filter copied files keeping the directory structure intact
```sh
rsync -av --include="*/" --include="*-pose.csv" --exclude="*" <source> <destination>
```
