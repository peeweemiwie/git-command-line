# git-command-line
### reset hard from remote branch
    git checkout [your-branch]
    git fetch origin [your-branch]
    git reset --hard origin/[your-branch]

### rebase - master from remote master
    git pull --rebase
    
### rebase - local branch from remote master
    git pull --rebase origin master
