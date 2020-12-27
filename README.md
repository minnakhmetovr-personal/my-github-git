## Git configuration

Edit the default configuration <br />
`git config --global -e`

Handling end of line character ["true" for Windows; "input" for linux] <br />
`git config --global core.autocrlf true`

## Working with a repository

Initialization of a new local repository <br />
`git init`

Staging the files <br />
`git add file1`                     #Track a single file
`git add file1 file2`               #Track multiple files separated with space
`it add .`                          #Track all files

Unstaging the files <br />
`git restore --staged file1`

Discarding the local changes <br />
`git restore file1`
`git clean -fd` 		            #Remove untracked files and directories

Restoring a file to its previous version <br />
`git rm file1`
`git rm --cached bin/` 				#Remove a file from the staging area. [Optionally with -r for recursive]
`git restore --source=HEAD~1 file1` #~1 means 1-commit before Head

Checking modifications <br />
`it diff --staged` 				    #To see modifications between working directory and staging area
`git diff` 						    #To see modifications between staging area and working directory

Commit <br />
`git commit -m "initial commit."`
`git show commit identifier`    #Get commit identifier using git log --oneline
`git show HEAD`
`git show HEAD~1`                   #One step earlier than HEAD
`git show HEAD~2`                   #Two steps earlier than HEAD

Clonning a repository <br />
`git clone`


## Working with branches
`git branch -a`                     #Checking the branches
`git branch feature/awsmsp-001`     #Creating a branch
`git checkout feature/awsmsp-001`   #Switching to the branch
`git checkout -b feature-2`         #Create a branch and switch to it
`git branch -d feature-1`           #Delete a branch

Merging branches <br />
`git checkout master`               #First switch to the branch you want to merge to
`git merge feature-1`               #Merging feature-1 to master

Push <br />
`git push origin master`                    #Push to remote master
`git push origin feature/awsmsp-001`        #Push to remote branch
`git push https://github.com/a.git master`  #Remote repo address and branch to push to

Configure an alias <br />
`git remote add origin https://github.com/minnakhmetovr-personal/my-first-repo.git`
`git push origin master`                    #Pushing using the alias

Checking remote <br />
`git remote -v`


## Working with History
`git log`
`git log --oneline`
`git log --topo-order --all --graph --date=local --pretty=format:'%C(green)%h%C(reset) %><(55,trunc)%s%C(red)%d%C(reset) %C(blue)[%an]%C(reset) %C(yellow)%ad%C(reset)%n'`

Links <br />
https://github.com/dahlbyk/posh-git#installation