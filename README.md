# git-command-line
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

##SSH

https://help.github.com/articles/about-two-factor-authentication/

    git remote remove origin;  git remote add origin git@github.com:account-name/repo-name.git
    
    
##Cloning an Existing Repository

    $ git clone git@github.com:nymag/repository-name.git
    
    
