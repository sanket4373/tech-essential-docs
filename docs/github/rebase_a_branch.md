## Git Rebase

Merge conflict is a very common problem developers run into in situations where multiple developers are working on a same piece of code/file and contribute one after the other. Usually the second person has to rebase to accomodate the changes being merged by the first person. A git rebase needs to be done during such situations.



1. Checkout the master branch(assuming that the default upstream branch where code gets merged is master)

        $ git checkout master  

2. Pull changes from upstream and origin repo:
        
        $ git remote update

3. Rebase your local master with that of upstream 

        $ git rebase upstream/master (you should be able to see similar output when the rebase command is executed)
        First, rewinding head to replay your work on top of it...
        Fast-forwarded develop to upstream/master.

4. Push the changes to your origin 

        $ git push 


5. Check the commit of the head of the master branch 

        $ git log (check the latest commit hash for upstream repo, you should be committing your code changes after his commit )

6. Checkout the branch you are working on already

        $ git checkout <branch-name>

7. Rebase your current branch with your updated local(origin) copy

        $ git rebase origin/master

8. Compare that your local(origin) repo's commit hash is same as the upstream repo's hash.

        $ git log 

9. You will find the merge conflicts at this stage, if there are no merge conflicts which means you are good. If there are merge conflicts in your files then resolve the merge conflicts and continue the rebase

        $ git rebase --continue

10. Finally, again confirm the commits on your branch, your own branch commit should come after the rebased commit which was pulled from upstream.

        $ git log
