## Updating your branch

#### Creating your own branch for a new feature/bugfix  

    
    $ git remote -v (To check if you have a local fork and a upstream set up)git $ checkout -b <branch-name> (this creates a new branch)
    $ git branch  (To make sure you are working on the desired branch)
    $ git add <file_name> (stage all your files)
    $ git commit -s (or -v)
    $ git push --set-upstream origin <branch_name>

#### updating your PR 

    $ git branch (To make sure you are working on the desired branch)
    $ git checkout <branch-name>
    $ git add <file_name>
    $ git commit --amend

#### Add your commit message with whatever changes you have made and save it and push it to your branch
  
    $ git push origin <branch-name> --force
