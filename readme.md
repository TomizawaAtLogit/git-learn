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
git checkout -f main

# git branch commands
git branch feature-branch  
git checkout feature-branch  
    M readme.md  
    Switched to branch 'feature-branch'

git checkout main M readme.md  
    Switched to branch 'main'  
    Your branch is up to date with 'origin/main'.

gti branch -b {new branch}  
git branch {new branch} {source branch}  

git add .  
git commit -m 'add new branch'  

git push --set-upstream origin feature-branch  
    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0) remote: remote: Create a pull request for 'feature-branch' on GitHub by visiting: remote: https://github.com/TomizawaAtLogit/git-learn/pull/new/feature-branch remote: To https://github.com/TomizawaAtLogit/git-learn.git * [new branch] feature-branch -> feature-branch branch 'feature-branch' set up to track 'origin/feature-branch'.

git push -u origin feature-branch  
git push  

git pull  

# github pull request
Checkout via the command line
If you do not want to use the merge button or an automatic merge cannot be performed, you can perform a manual merge on the command line. However, the following steps are not applicable if the base branch is protected.

Step 1 Clone the repository or update your local repository with the latest changes.
git pull origin main  

Step 2 Switch to the head branch of the pull request.  
git checkout feature-branch

Step 3 Merge the base branch into the head branch.  
git merge main

Step 4 Fix the conflicts and commit the result.

See Resolving a merge conflict using the command line for step-by-step instructions on resolving merge conflicts.  
Step 5 Push the changes.  
git push -u origin feature-branch

=======
git checkout -f main  

2. after merged, delete branch by github ui    
git checkout main  
git pull origin main  
    From https://github.com/TomizawaAtLogit/git-learn
    * branch            main       -> FETCH_HEAD
    Updating 09d950d..fd9c30e
    Fast-forward
    readme.md | 44 +++++++++++++++++++++++++++++---------------
    1 file changed, 29 insertions(+), 15 deletions(-)

git log --oneline

1. Clone the repogitory  
2. Create a new branch from the main or another branch  
3. Make your changes  
4. Push the branch to the remote repo  
5. Open a Pull Request  
6. Merge the changes  
7. Pull the merged changes into your main branch  
8. Repeat from step 2  

# Solve merge confrict
git checkout main  
git pull  

git checkout {merged-branch}  
git merge main  

# git reset
this line will be deleted.
This line also will be deleted.

git add .  
git commit -m 'reset 1'  
git log --oneline  
git reset 3a19e51{commit hash}  
git status  
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to disc

# git revert
1. change code  
git log --oneline  
git revert 2830863  
    Auto-merging readme.md
    CONFLICT (content): Merge conflict in readme.md
    error: could not revert 2830863... finalyze reset
    hint: After resolving the conflicts, mark them with
    hint: "git add/rm <pathspec>", then run
    hint: "git revert --continue".
    hint: You can instead skip this commit with "git revert --skip".
    hint: To abort and get back to the state before "git revert",
    hint: run "git revert --abort".
    hint: Disable this message with "git config advice.mergeConflict false"

git status
    On branch main
    Your branch is ahead of 'origin/main' by 2 commits.
    (use "git push" to publish your local commits)

    nothing to commit, working tree clean

This is a urgent bugfix.

# git stash
git branch dev-tomizawa  
git checkout dev-tomizawa  
    Switched to branch 'dev-tomizawa'

git push --set-upstream origin dev-tomizawa  
    Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    remote: 
    remote: Create a pull request for 'dev-tomizawa' on GitHub by visiting:
    remote:      https://github.com/TomizawaAtLogit/git-learn/pull/new/dev-tomizawa
    remote:
    To https://github.com/TomizawaAtLogit/git-learn.git
    * [new branch]      dev-tomizawa -> dev-tomizawa
    branch 'dev-tomizawa' set up to track 'origin/dev-tomizawa'.



This is a urgent bugfix.
