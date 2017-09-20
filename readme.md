# **SUMMARY**

**REPOSITORY** - collection of related items, or files related to a software project.  
**GIT REPOSITORY** - folder or items being tracked by Git.  
**VERSION CONTROL** - tracking of files added, removed, modified, who did it.

### CONFIGURE GIT

| Command |   |
| ------- | - |
| git --version | check if git was installed |
| git config --global user.name "your name" | set your name |
| git config --global user.email "your email" | set your name |

### CREATING LOCAL REPO

| Command |   |
| ------- | - |
| mkdir <folder-name> | Make a new folder (aka make directory) |
| cd <folder-name> | Navigate into an existing folder (aka change directory) |
| ls | List the items in a folder |
| git init | initialize git |

### COMMIT (aka SAVE)

| Command |   |
| ------- | - |
| git status | Check status of changes to a repository |
| git diff | View changes to files |
| git add <file-name> | Add a file's changes to be committed |
| git add . | To add all files changes |
| git commit -m "your commit message" | Commit (aka save) the changes you've added with a short message describing the changes |

### **GITHUB BIN**

| Command |   |
| ------- | - |
| git config --global user.username <username> | Add your Github username to your git configuration |
| git config --global user.username | Double check what you have set in your git config |

**_NOTE:_**
Make sure you type "user.username" above and not "user.name", which would override the name you set in the first challenge and leave you with no username property! If you found you did that, it's ok, just repeat the step in the first challenge to add your name.


### **REMOTES**

REMOTE REPO - putting your repos on Github. Those repos lives on one of Github's servers.

By PUSHING your local (on your computer) changes to it, you keep it up to date.
Others can always get the latest from your project by PULLING your changes down from the remote (and onto their computer).

-----

CREATE REMOTE REPO:
1. Go to github.com, log in and click the '+' in the top right and then click 'New repository'.
2. Give it a name that matches your local repo's name and a short description.
3. Make it public. This means it will be listed on your public profile.
4. Don't initialize with a README because we already have a file, locally, named 'readme.txt'.
5. Leave '.gitignore' and 'license' set to 'none'. (It will not be used in this tutorial)
6. Click create repository

-----

CONNECT LOCAL REPO TO REMOTE REPO:
1. On github, copy the address/url showed on Quick setup. Make sure the https button is selected.
2. git remote add origin <URL-FROM-GITHUB>	- Add a remote named 'origin' to your repo:

(Your local repo now knows where your remote repo named 'origin', lives on github. Think of it as adding a name and address on your speed dial - now when you need to send something there, you can.)

-----

PUSH WORK TO YOUR REMOTE:
Next, you want to push (send) everything you've done locally to your remote repo on Github. This is something you'll do often so that your remote version is up to date and matching the state of your local version.

3. git push origin master

origin - the name given to your remote repo
master - the name given to your local repo

-----

git remote add <REMOTE-NAME> <URL>	    - Add remote connections
git remote set-url <REMOTE-NAME> <URL>	- Set a URL to a remote (FOR WINDOWS)
git pull <REMOTE-NAME> <BRANCH-NAME>	  - Pull in changes
git remote -v				                    - View remote addresses
git push <REMOTE-NAME> <BRANCH>		      - Push changes

------------------------------

FORKS AND CLONES

-----

FORK Repo   - creating a copy of other'r repo on your github account.
CLONE Repo 	- getting a forked repo from your github and save it to your computer.

-----

CLONE A FORKED REPO:
1. Make sure you're not inside a local repo. If inside a repo, exit by changing directory one level.
2. git clone <URL-FROM-GITHUB>	- clone your forked repo.
3. cd <CLONED-REPO-FOLDER>	    - go to the folder it created by changing directory.
4. git remote -v		            - Check remote address setup (should have origin)

-----

CONNECT TO ORIGINAL REPO:
Original repo might change, you need to pull those changes.

1. git remote add upstream <ORIG-FORKED-REPO-URL>
2. git remote -v					                        - check remote address setup (should have
							                                      origin and upstream)

upstream - name given for orig repo

------------------------------

BRANCHES
used to isolate and continue work when needed without affecting the main branch named master.

-----

CREATE BRANCH
1. git status
2. git branch <BRANCH-NAME>
3. git checkout <BRANCH-NAME>
4. Add changes and update branch
	git status
	git add .
	git commit -m "message"
5. git push origin <BRANCH-NAME>

-----

git checkout -b <BRANCH-NAME>	  - Create and switch to a branch in one line.
git branch <BRANCH-NAME>	      - Create a new branch.
git checkout <BRANCH-NAME>	    - Move onto a branch.
git branch			                - List the branches.
git branch -m <NEW-BRANCH-NAME>	- Rename a branch you're currently on.
git status			                - Verify what branch you're working on.

------------------------------

MERGE BRANCH
1. git checkout master					                  - move into main branch
2. git merge <BRANCH-NAME> 				                - merge a branch to main branch
3. git branch -d <BRANCH-NAME>				            - delete the branch you merged
4. git push <REMOTE-NAME> --delete <BRANCH-NAME>  - Delete a remote branch.

-----

git merge <BRANCHNAME>				              - Merge a branch into current branch.
git checkout <BRANCHNAME>			              - Change the branch you're working on.
git branch -d <BRANCHNAME>			            - Delete a local branch.
git push <REMOTENAME> --delete <BRANCHNAME>	- Delete a remote branch.

------------------------------

PULL
You need to stay up to date with the latest changes if you're working on a project with someone else.

git pull <REMOTE-NAME> <BRANCH-NAME>	- Pull in changes from a remote branch.
git fetch --dry-run			              - See changes to the remote before you pull in.

------------------------------
