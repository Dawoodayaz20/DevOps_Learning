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
    * What it does is : "It tells git what did you do and when you did it. ust like creating a copy of your project at that time. So in the future, if you want you can revert to that old commit. 
    * It is the last step towards pushing your code to your remote repo.
  - git remote add origin "The link to the remote repo"
    * Command for connecting your local repo to remote repo.
  - git push -u origin main
    * Command for pushing your code to remote repo.