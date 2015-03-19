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
