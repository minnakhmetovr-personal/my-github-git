## Git configuration

Edit the default configuration <br />
`git config --global -e` <br />

Handling end of line character ["true" for Windows; "input" for linux] <br />
`git config --global core.autocrlf true`<br />

## Working with a repository

Initialization of a new local repository <br />
`git init`<br />

Staging the files <br />
`git add file1`        #Track a single file <br />
`git add file1 file2`  #Track multiple files separated with space <br />
`it add .`             #Track all files <br />

Unstaging the files <br />
`git restore --staged file1` <br />

Discarding the local changes <br />
`git restore file1`
`git clean -fd`        #Remove untracked files and directories <br />

Restoring a file to its previous version <br />
`git rm file1` <br />
`git rm --cached bin/`              #Remove a file from the staging area. [Optionally with -r for recursive] <br />
`git restore --source=HEAD~1 file1` #~1 means 1-commit before Head <br />

Checking modifications <br />
`it diff --staged`                  #To see modifications between working directory and staging area <br />
`git diff`                          #To see modifications between staging area and working directory <br />

Commit <br />
`git commit -m "initial commit."` <br />
`git show commit identifier`        #Get commit identifier using git log --oneline <br />
`git show HEAD`
`git show HEAD~1`                   #One step earlier than HEAD <br />
`git show HEAD~2`                   #Two steps earlier than HEAD <br />

Clonning a repository <br />
`git clone` <br />


## Working with branches
`git branch -a`                     #Checking the branches <br />
`git branch feature/awsmsp-001`     #Creating a branch <br />
`git checkout feature/awsmsp-001`   #Switching to the branch <br />
`git checkout -b feature-2`         #Create a branch and switch to it <br />
`git branch -d feature-1`           #Delete a branch <br />

Merging branches <br />
`git checkout master`               #First switch to the branch you want to merge to <br />
`git merge feature-1`               #Merging feature-1 to master <br />

Push <br />
`git push origin master`                    #Push to remote master <br />
`git push origin feature/awsmsp-001`        #Push to remote branch <br />
`git push https://github.com/a.git master`  #Remote repo address and branch to push to <br />
`git push --set-upstream origin my-branch`  #Push to a remote branch, creating one first. <br /> 

Configure an alias <br />
`git remote add origin https://github.com/minnakhmetovr-personal/my-first-repo.git` <br />
`git push origin master`                    #Pushing using the alias <br />

Checking remote <br />
`git remote -v` <br />


## Working with History
`git log` <br />
`git log --oneline` <br />
`git log --topo-order --all --graph --date=local --pretty=format:'%C(green)%h%C(reset) %><(55,trunc)%s%C(red)%d%C(reset) %C(blue)[%an]%C(reset) %C(yellow)%ad%C(reset)%n'` <br />

Links <br />
https://github.com/dahlbyk/posh-git#installation <br />
https://docs.aws.amazon.com/codecommit/latest/userguide/how-to-conditional-branch.html #CodeCommit - Limit Pushes<br />