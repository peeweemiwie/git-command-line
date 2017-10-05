# git-command-line

### search branch name using `grep`
`git branch --all | grep <id>`

### reset hard from remote branch
    git checkout [your-branch]
    git fetch origin [your-branch]
    git reset --hard origin/[your-branch]

### rebase - master from remote master
    git pull --rebase
    
### rebase - local branch from remote master
    git checkout [your-branch]    
    git fetch origin  
    git rebase origin/master 
    git push origin[your-branch]

##### Then push to remote. 
    git push -f origin [your-branch]

### Discard changes in local working direcotry
    git checkout -- filename

### View difference between your files and HEAD: 
    git diff HEAD

### Differenct between `git pull` and `git fetch`
http://git-scm.com/docs/git-pull

http://git-scm.com/docs/git-fetch

Great comment found on stackoverflow : http://stackoverflow.com/questions/292357/what-are-the-differences-between-git-pull-and-git-fetch

In the simplest terms, `git pull` does a `git fetch` followed by a `git merge`.

You can do a `git fetch` at any time to update your remote-tracking branches under `refs/remotes/<remote>/`. This operation never changes any of your own local branches under `refs/heads`, and is safe to do without changing your working copy. I have even heard of people running git fetch periodically in a cron job in the background (although I wouldn't recommend doing 
this).

A `git pull` is what you would do to bring a local branch up-to-date with its remote version, while also updating your other remote-tracking branches.

##SSH two factor authentication

https://help.github.com/articles/about-two-factor-authentication/

    git remote remove origin;  
    git remote add origin git@github.com:account-name/repo-name.git
    
    
##Cloning an Existing Repository

    $ git clone git@github.com:nymag/repository-name.git
    
##Rename local branch

To rename other branch

    git branch -m <oldname> <newname>

To rename the current branch

    git branch -m <newname>


##Ignore local change

    git checkout -f

##Roll back to commit id

    git reset --hard c14809fa
    
It will make your local code and local history be just like it was at that commit. But then if you wanted to push this to someone else who has the new history, it would fail.

if you do

    git reset --soft c14809fa
It will make your local files changed to be like they were then, but leave your history etc. the same.
http://stackoverflow.com/questions/3639115/reverting-to-a-specific-commit-based-on-commit-id-with-git


##Amending the commit message

    git commit --amend -m "New commit message"
    
## Remove directory

    git rm -r one-of-the-directories
    git commit -m "Remove duplicated directory"
    git push origin master

## Git stash

    $ git status
    $ git stash list
    stash@{0}: WIP on master: 049d078 added the index file
    stash@{1}: WIP on master: c264051 Revert "added file_size"
    stash@{2}: WIP on master: 21d80a5 added number to log
    $ git stash apply
    or
    $ git stash apply stash@{2}
    
    
    ls -ahl
    
    history
    
    command + r

## Add all files to a commit except a single file?

http://stackoverflow.com/questions/4475457/add-all-files-to-a-commit-except-a-single-file

    git add -u
    git reset -- main/dontcheckmein.txt
