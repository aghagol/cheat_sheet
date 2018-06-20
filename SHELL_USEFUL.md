### Useful commands for Shell, Bash, ...

Filter copied files keeping the directory structure intact
```sh
rsync -av --include="*/" --include="*-pose.csv" --exclude="*" <source> <destination>
```

Nicer command prompt colot scheme, showing git branch at prompt
```sh
PS1='\[\033[0;32m\]\[\033[0m\033[0;32m\]\u\[\033[0;36m\] @ \[\033[0;36m\]\h \w\[\033[0;32m\]$(__git_ps1)\n\[\033[0;32m\]└─\[\033[0m\033[0;32m\] \$\[\033[0m\033[0;32m\] ▶\[\033[0m\] '
```
