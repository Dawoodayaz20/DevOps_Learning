## Commands for git
- git init
  * This command will initialize git in your folder and after this, git will keep track of your files.
- git add .
  * For staging all tracked files.
- git status
  * This command will show on which branch you are, and any files if untracked.
- git branch -M main
  * Command for specifying the branch in git
- git commit -m "The message telling what will this commit do."
  * For committing the staged files with a commit message.  
  * What it does is : *It tells git what did you do and when you did it. ust like creating a copy of your project at that time. So in the future, if you want you can revert to that old commit*. 
  * It is the last step towards pushing your code to your remote repo.
- git remote add origin *The link to the remote repo*
  * Command for connecting your local repo to remote repo.
- git push -u origin main
  * Command for pushing your code to remote repo.
- git log
  * This command shows the history of commits with:
    1. Commit id
    2. Author: Name and email id of the person commit
- git checkout *Then the id of your commit*.
  * This command will switch you back to your older commit. 
  * In git, there is a concept of HEAD that points to the latest commit you are on, and when you switch to an older commit. You will see a message saying:
    - You are in detached HEAD.
    - HEAD is now at *commitID* *commit message*.
  * The git checkout command didn't delete the files, rather it just moved the HEAD to a previous state. 
  * After this, if u want to move to a stable state, run:
    - git checkout main:
      This will move you to that current branch
- git branch *branch-name*
  * This command will create a new branch
- git checkout *branch-name*
  * This command is to switch to another branch.
  *Note:*
    - The branch that you created will inherit the code from the branch you were on previously. If you are on main branch and you created master branch, it will inherit the code from main branch. 