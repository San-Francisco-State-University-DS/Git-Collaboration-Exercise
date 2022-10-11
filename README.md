# Git-Collaboration-Exercise
Please make your own branch from this main repo and add your update to the main branch.


## New Branch Process:

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

## Fetch, Commits, Pull Request

1. Fetch a Remote Branch

When a new development branch is created by your team member, we can fetch the new remote branch to a local repository.  It's not an often case that you need all the development branches fetched to the local repo.  One of the most common cases is that a tema member needs the code source from another member to continue his/her work.  If collaboration code is not needed, try to avoid fetching other branches to the local repo when working on a specific dev branch for your assigned task.

Terminal:

``` sh
git fetch origin <name of branch> # fetching all updated remote branches to the local repo
git branch  # Check to see if the branch is fetched
git checkout <name of branch>
```

2. Commits

When a task is assigned to a member in a team, one can commit and push changes to his/her remote dev branch as many time as needed.  The best practice is to commit as frequent as possible for the completed steps within the scope fo the assigned task. 

e.g. A member is assigned a task to complete 5 data visualization by the end of the week.  First, this member should create a dev branch for this task. While the member is working on this task, he/she **SHOULD** commit the changes after each visual is created. The benefit for committing changes frequently is to better define a version of the source code so when something went wrong, he/she can chase back to the most recent version of the repo.

Note that the member does not need to push every commit to the remote dev branch, but they should push a bunch of commits at once to the remote.  For example, commit 3 visuals one by one, then push all 3 commits to the remote dev branch all at once.

Terminal:

``` sh
git add .  # or specify a specific file
git commit -m 'message for the update'  # be as specific as possible

## After several commits, they can all be packed in a single push
git push --set-upstream origin <name of branch>
git log --all --graph # Check the log for all commits to the remote dev branch
```

3. Pull Request

Once a member completed a task that was assigned by a team, he/she should 1) push all final updates to the remote dev branch, 2) submit a pull request for the final version of the dev branch, and 3) inform the team to assign a member to review and make comment on the code source and approve for merging the code.  

Note that no one should ever approve their own code and merge to the main branch.  Imagine a member accidentally approve his/her own code and merge the branch to main without noticing the rest of the team.  It could cause a big mess while others are merging their code to the main branch later (merge conflict, incorrect version of package for the analysis, incorrect data source directory, etc).  Therefore, the team needs to communicate well to avoid any kind of conflict of merging their code.  Remember, the ```origin main``` branch is the final version of the project.  No one should have the right to merge their dev branch into ```main```.

The good practice could be scheduling a code review section once a pull request is submitted.  A member in the team will review and comment on the updates.  If revision is needed, send message to the member who submitted the pull request and have he/she review the code source.  Once the final version is reviewed, the review member can then inform another member in the team to approve the pull request so the dev branch can finally merged into the ```main```.  

GitHub provides some nice UI for the pull reqeust revision.  Check out the documentation from GitHub for detail. 


