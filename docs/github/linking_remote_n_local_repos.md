### Linking your local fork to a upstream repo


1. Fork the repo which you want to work on by pressing fork button on github.com

2. Git clone your fork

        $ git clone git@github.com:username/upstream-repo-name.git

3. change to go in the repository

        $ cd upstream-repo-name

4. Now we link our local repo to the central (upstream repo) in order to pull changes from there
    
        $ git remote add upstream git@github.com:upstream-repo-name/upstream-repo-name.git
    

5. Now, verify if the remote is indeed been added
	
        $ git remote -v
