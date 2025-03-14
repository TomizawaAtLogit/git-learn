### GIT command

## set up  
1. make new ropogitory on github

2. follow the guidance  
…or push an existing repository from the command line

git remote add origin https://github.com/TomizawaAtLogit/git-learn.git  
git branch -M main  
git push -u origin main  
    error: failed to push some refs to 'https://github.com/TomizawaAtLogit/git-learn.git'

3. make a readme.md file  
4. make a .gitignore file  
touch .gitignore

# commit file and push commands
git add .  
git commit -m "add readme"

git push

    fatal: The current branch main has no upstream branch.  
    To push the current branch and set the remote as upstream, use

        git push --set-upstream origin main

    To have this happen automatically for branches without a tracking  
    upstream, see 'push.autoSetupRemote' in 'git help config'.

git push --set-upstream origin main

    Enumerating objects: 4, done.  
    Counting objects: 100% (4/4), done.  
    Delta compression using up to 12 threads  
    Compressing objects: 100% (2/2), done.  
    Writing objects: 100% (4/4), 272 bytes | 272.00 KiB/s, done.  
    Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)  
    To https://github.com/TomizawaAtLogit/git-learn.git  
    * [new branch]      main -> main  
    branch 'main' set up to track 'origin/main'.

# git log and status commands
git log  
git log --oneline  
git status  

# git checkout commands
git log --oneline  
git checkout {commit number}  
    Note: switching to 'ec148a8'.

    You are in 'detached HEAD' state. You can look around, make experimental
    changes and commit them, and you can discard any commits you make in this
    state without impacting any branches by switching back to a branch.

    If you want to create a new branch to retain commits you create, you may
    do so (now or later) by using -c with the switch command. Example:

    git switch -c <new-branch-name>

    Or undo this operation with:

    git switch -

    Turn off this advice by setting config variable advice.detachedHead to false

    HEAD is now at ec148a8 add articles on readme

git checkout main  




