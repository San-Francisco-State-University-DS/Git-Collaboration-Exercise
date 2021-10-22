# Git-Collaboration-Exercise
Please make your own branch from this main repo and add your update to the main branch.


Process:

1. Clone this repository to your local machine.

Terminal:

``` sh
cd ~/.../project_folder
git clone <SSH>

OR

git clone <HTTPS>

cd <Repo Name>
```

2. Create and checkout the branch of this repository

Terminal:

``` sh
git branch <name of branch>
git checkout <name of branch>
```

3. Add the modified file(s) to the branch

Terminal:

``` sh
git add .
git commit -m "message for the update"
git log --all --graph
```

4. Merge the branch to the main repository on GitHub

Terminal:

``` sh
git checkout main
git merge <name of branch> -m "message for the update"

OR

git push -u origin <name of branch>

git log --all --graph
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

8. Update Local Repository

Terminal:

``` sh
git fetch 
git log --all --graph
git pull origin main
git log --all --graph
```
