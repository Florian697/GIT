# GIT Cheat Sheet:

---

#Initial setup:

| Command                                                        | Description                                                                 |     example                                              
|----------------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------
|git config --global user.name "[name]"                          |Sets the name that will appear in the author field for the commits you make  |git config --global user.name "My Name"    
|git config --global user.email "[E-mail address]"               |Specifies the email address that will be used for all commits                |git config --global user.email “namet@gmail.com”          
|git remote                                                      |Allows you to manage connections to repositories                             |git remote set-url origin ssh://git@github.com/DevOps.git 

---

#Basic Operations:

| Command                                                        | Description                                                                  |     example                    
|----------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------
|git init [project name]                                         |Creating a repository in the current directory                                |git init my_cool_project
|git clone [url-address]                                         |Download remote repository                                                    |git clone https://github.com/DevOps.git; git clone git@github.com:DevOps.git;

---

#Synchronization with a remote repository:

| Command                                                        | Description                                                                                   |     example                                                                  
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|--------------------------------
|git fetch [remote repository]                                   |Downloads history from a remote repository                                                     |
|git push [remote repository] [branch]                           |Uploads all changes from the local branch to the remote repository                             |
|git pull                                                        |Loads history from a remote repository and merges it with the local one. pull = fetch + merge  |git pull

---

#Alteration:

| Command                                                        | Description                                                                                   |     example                    |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|--------------------------------|
|git status                                                      |Lists all new or changed files that need to be committed to the index                          |git status
|git add [file]                                                  |Adding files to Index                                                                          |git add index.html; git add . ; git add --all ;
|git rm [file]                                                   |Removes a file from the working directory and indexes its deletion                             |git rm index.html
|git rm --cached [file]                                          |Removes a file from version control, but physically leaves it in its place                     |git rm --cached index.html
|git mv [original file] [new name]                               |Moves or renames a file, immediately indexing it for a later commit                            |git mv index.html index.txt
|git diff                                                        |Shows differences in changes made in files that have not yet been indexed                      |git diff
|git diff --staged                                               |Shows differences between indexed and last committed versions of files                         |git diff --staged
|git log --follow [file]                                         |History of changes to a specific file                                                          |git log --follow index.txt

---

#Commits

| Command                                                       | Description                                                                                   |     example                    |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------|--------------------------------|
|git commit -m "[commit description]"                           |Captures indexed changes and saves them to version history                                     |git commit -m "Added new feature."
|git commit –amend -m "new commit description"                  |Changing the last commit message                                                               |git commit –amend -m "Added new feature. Task in Jira 3247"
|git log                                                        |View project changes (commits)                                                                 |git log
|git show [commit number]                                       |Prints information and shows changes in the selected commit                                    |git show 73b64290a107f6325ab88c7950637a4ce44c42a6
|git reset [commit number]                                      |Undoes all commits after the specified one, leaving all changes in the working directory       |git reset 73b64290a107f6325ab88c7950637a4ce44c42a6
|git reset --hard [commit]                                 |Resets the entire history along with the state of the working directory before the specified commit.|git reset --hard 73b64290a107f6325ab88c7950637a4ce44c42a6
|git log --graph --oneline --stat                               |Viewing project changes (commits) as a graph                                                   |git log --graph --oneline --stat

---

#Branching:

| Command                                                       | Description                                                                                   |     example                    |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------|--------------------------------|
|git branch                                                     |List of commit branches                                                                        |git branch
|git branch [name branch]                                       |Create a new branch                                                                            |git branch feature1
|git checkout [name branch]                                     |Switch to selected branch                                                                      |git checkout feature1
|git branch -d [name branch]                                    |Delete selected branch                                                                         |git branch -d feature1
|git branch –m [startштп name branch] [new name branch]         |Renaming a branch                                                                              |git branch –m feature1 SuperButtonFeature
|git merge [name branch]                                        |Merge branches (brings changes from the specified branch into the current branch)              |git merge hotfix
|git push origin --delete [name branch]                         |Delete a branch on the server                                                                  |




