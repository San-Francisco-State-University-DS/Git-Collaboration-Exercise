# Git-Collaboration-Exercise
Please make your own branch from this main repo and add your update to the main branch.


Process:

1. Clone this repository to your local machine.

Terminal:

``` sh
cd ~/.../project_folder

git clone <SSH> # if using SSH key

OR

git clone <HTTPS> # if using PAT

cd <Repo Name>
```

2. Create and checkout the branch of this repository

Terminal:

``` sh
git branch <name of branch>. # create a new branch locally
git checkout <name of branch> # swich to the new created branch
```

3. Add the modified file(s) to the branch

Terminal:

``` sh
git add .  # add any update to the new branch
git commit -m "message for the update"  # commit the change with a message
git log --all --graph  # check the staging status in the new branch
```

4. Merge the branch to the main repository on GitHub

Terminal:

``` sh
git checkout main  # switch back to main branch locally
git merge <name of branch> -m "message for the update"  # merge the changes in new branch to main locally
git push -u origin <name of branch>  # push the change from new branch to the remote, namely "origin"
git log --all --graph  # check all the log status 
```

Alternative, when the local branch is not connected with the remote origin,

``` sh 
git push --set-upstream origin <name of branch>
```

5. Create a Pull Request on GitHub

Go back to the GitHub remote repository and check to see if the branch is created.
Click on the green "Pull Request" button to create a pull request.
OR
Click on "Pull request" tab at the top of the repository and click the green "Create pull request" button.

6. Review and discuss the changes

Review the code from the author of this branch.

7. Approve the merge

Merge the branch once the team agrees to the update.

8. Update Local Repository (ONLY IF the change has not been merged locally!!)

Terminal:

``` sh
git fetch 
git checkout main
git log --all --graph
git pull origin main
git log --all --graph
```
