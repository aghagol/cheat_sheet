First clone bare repo:

```sh
git clone --bare https://github.com/user/repo.git
```

Then run the following script in the repo:

```sh
#!/bin/sh

git filter-branch --env-filter '

OLD_EMAIL="a@b.c"
CORRECT_NAME="abc"
CORRECT_EMAIL="c@d.e"

if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
```

Finally, push the changes:

```sh
git push --force --tags origin 'refs/heads/*'
```

