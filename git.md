<h3>Gig Commands:</h3>


  - https://github.com/typicode/husky/issues/1014

  - git commit -m "message" --no-verify


git log --graph --oneline --all --decorate

git clean -xfd

You don't have to modify the .gitignore: you can force the addition of those files:

force the addition of files included in .gitignore

git add --force -- file1 file2

<b>Delete the most recent commit:</b>

git reset --hard HEAD~1

<b>Delete the most recent commit, without destroying the work you've done:</b>

git reset --soft HEAD~1

<b>Unstage:</b>

git reset -- example.txt


git push -u origin {local branch name}

git config --global alias.s status

git config --global alias.cm checkout master

git config --global alias.c checkout


git submodule update --remote {sub module name}

<b>How to tidy up your merge requests with Git</b>
https://about.gitlab.com/2019/02/07/start-using-git/


