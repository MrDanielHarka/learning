# Git

## Notes

### General


### Commands

- **git clone git@github.<span>com:USER-NAME/REPOSITORY-NAME.git** : We can clone an online repo with SSh to have it locally.
- **git remote -v** displays repo URL.
- **git status** tells us the status of the repo.
- **git add file.<span>md** adds the file to the staging area in.
- **git add .** adds all files in directory to staging area.
- **git commit -m "Add file.<span>md"** One or more files will be commited.
- **git log** shows us the logs of the changes.
- **git branch branchName** creates a new branch.
- **git checkout branchName** lets us cd to an other branch.
- **git branch** logs the available brances and marks current one with * symbol.
- **git branch -a** includes remove repos in list.
- **git push origin main** uploads commited file(s) to GitHub.
- **git fetch http** downloads remote repo locally.
- **git branch -d branchName** deletes local branch
- **git push origin --delete branchName** deletes remote repo.
- **git pull** shorthand for fetch + merge.
- **git checkout -b newBranch** creates a new branch and cds there.
- **git commit -a -m "message"** adds file to staging area and commits it.
- **git pull --rebase** Pulls then rebases repo.
- **git diff** shows the changes made.
- **git stash save "some message"** savesw current state.
- **git stash list** Shows the list of stashes.
- **git stash apply stash@{0}** recovers past changes.