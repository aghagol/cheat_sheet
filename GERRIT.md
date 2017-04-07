```sh
git reset --hard #restores repo when files deleted
git pull --rebase origin master
git reset <file> #undo git add
git commit --amend #amend patch
git push origin HEAD:refs/for/master%topic=TMOD-lib,r=<email>
git reflog #to know the reference I want in HEAD
git reset --hard HEAD{<ref log>}
git pull --rebase origin master 
git reset --hard HEAD~1 #cancel commits
git reset --hard origin/master
```
