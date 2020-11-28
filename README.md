######GIT COMMANDS

[Visual Git Cheat Sheet ](http://ndpsoftware.com/git-cheatsheet.html#loc=stash;)

[Git Documentation](https://git-scm.com/docs)

[Setting up a repository help tutorial](https://www.atlassian.com/git/tutorials/setting-up-a-repository)


----------------------------------------------------------------------------------------------------------------------------------------
### CONFIGURE TOOLING
Configure user information for all local repositories

- git --version						                                           ( Check Version )

- git config --global user.name "[name]"                             ( Sets the name you want atached to your commit transactions )

   - git config user.email					                                     ( Show email )

- git config --global user.email "[email-address]"                   ( Sets the email you want atached to your commit transactions )

   - git config user.name                                               ( Show username )

- git config --global color.ui auto                                  ( Enables helpful colorization of command line output )

- git config --list					                                         ( List of all Config )

- git help [Command]					              	 ( Show help for the command )

- git config --global alias.[shortcut] [command]      ( Aliases are used to create shorter commands that map to longer commands )

- git config --system core.editor [editor]            ( Set text editor used by commands for all users on the machine )

- git config --global --edit                          ( Open the global configuration file in a text editor for manual editing )


----------------------------------------------------------------------------------------------------------------------------------------
### Create Repositories
Start a new repository or obtain one from an existing URL

- $ git init                                        ( Transform the current directory into a Git repository )

  - git init [project-name]			                ( Creates a new local repository with the specified name )

  - git init [directory]                            ( Create an empty Git repository in the specified directory )

- $ git clone [repo-url]                            ( Downloads a project and its entire version history from repo to local machine )

- git remote add [RemoteRepoName] [Repo-url]		    ( Create a new connection to a remote repo ) 

  - git remote								                ( Shows info about the remote repo )


----------------------------------------------------------------------------------------------------------------------------------------
### Make Changes
Review edits and craf a commit transaction

- git status                ( Lists which files are staged, unstaged, and untracked )

- git diff                  ( Show unstaged changes between your index and working directory )

  - git diff --staged       ( Shows file differences between staging and the last file version )

  - git diff HEAD           ( Show difference between working directory and last commit )

  - git diff --cached       ( Show difference between staged changes and last commit )    

  - git diff [first-branch]...[second-branch]	( Shows content differences between two branches )

- git add . // git --all    ( Stage all the changes )

  - git add -p              ( Review each of the changes , and select which change is goning to be staged )

  - git add *.txt           ( Stage all txt files in current directory )

  - git add *.html          ( Stage all html files in current directory )

  - git add [File]          ( Stage current file in preparation for next commit )

  - git add [Directory]     ( Stage all changes in directory for next commit )

- git commit -m "Message]"   ( Records file snapshots permanently in version history )

  - git commit -am "Message" // git commit -a -m "MESSAGE"	( Adds changes and Commit in same time )

  - git commit --amend -m "Message"	 ( Replace the last commit with the staged changes and last commit combined )
  
  - git commit --fixup [commitID]   ( Fix an old commit )

- git rebase [base]         ( Rebase the current branch onto base. Base can be commit ID, Branch name, tag, Master )

 
----------------------------------------------------------------------------------------------------------------------------------------
### Group Changes
Name a series of commits and combine completed efforts

- git branch					        ( Lists all local branches in the current repository )

  - git branch [Branch-name]			    ( Creates a new branch )

  - git checkout [Branch-name]           	( Switches to the specified branch and updates the working directory )

  - git checkout -b [Branch-name]           ( Create and switch to a new branch)

  - git branch -d [branch-name]			( Deletes the specified branch )

- git checkout [commit ID]          ( View older commit. Working directory match exact state of the ID commit )


----------------------------------------------------------------------------------------------------------------------------------------
### Refactor Filenames
Relocate and remove versioned files

- git rm [file]					            ( Deletes the file from the working directory and stages the deletion )

- git rm --cached [file]			        ( Removes the file from version control but preserves the file locally )

- git mv [file-original][file-renamed]		( Changes the file name and prepares it for commit )


----------------------------------------------------------------------------------------------------------------------------------------
### Review History
Browse and ispect the evolution of project files

- git log					( Display the entire commit history for the current branch, Check what branch you are currently on )

  - git log --oneline --decorate --all --graph      ( Compresed view with decoration and art )

  - git log --follow [file]			( Lists version history for a file, including renames )

  - git log --author="[User]"			( Lists commit from specific user )

  - git log [File]                  ( Lists commit that include specific file )
 
- git show HEAD					( Show the most recently commit HEAD )

- git show [commit]				( Outputs metadata and content changes of the specified commit )


----------------------------------------------------------------------------------------------------------------------------------------
### Undo Mistakes
Erase mistakes and craft replacement history

- git restore .             ( Discard all uncommited changes, 
   
   - git restore [Filename]      ( Discard uncommited local changes to a file, also works for deleted files )

- git reset [commitID]				( Undoes all commits after [commit], sets the pointer head to commitID )

  - git reset --hard [commitID]		( Discard all history and changes back to the specified commit, deletes local changes )
  
  - git reset --mixed [commitId]    ( Discard all history and changes back to specified commit, keeps local changes )

  - git reset -p                    ( Unstange individual changes )

  - git reset HEAD [Filename]		( Remove file from staging area )

  - git reset --hard HEAD^			( Undo last commit, and all changes )

  - git reset --hard HEAD^^			( Undo last 2 commits, and all changes )

  - git reset --soft HEAD^			( Undo last commit, put changes into stagin )

  - git reset [File]          ( Unstages the file, but preserve its contents )

- git revert [commitID]            ( Create new commit that undoes all of the changes in commitID, than apply it to the current branch )

  - git revert HEAD              ( HEAD will revery the latest commit )

- git clean -n                   ( Shows which untracked files are going to be removed without actually removing them )

  - git clean -f                 ( Initiates the actual deletion of untracked files )


----------------------------------------------------------------------------------------------------------------------------------------
### Save Fragments
Shelve and restore incomplete changes

- git stash					( Temporarily stores all modified tracked files )

- git stash pop					( Restores the most recently stashed files )

- git stash list				( Lists all stashed changesets )

- git stash drop				( Discards the most recently stashed changeset )


----------------------------------------------------------------------------------------------------------------------------------------
### Synchronize Changes
Register a repository bookmark and exchange version history

- git fetch [bookmark]				    ( Downloads all history from the repository bookmark )

- git merge [bookmark]/[branch]			( Combines bookmark`s branch into current local branch )

- git merge [Branch]	                ( Combines the specified branch’s history into the current branch )

- git push [Remotename] [branch]		( Uploads all local branch commits to GitHub )

- git pull [Remotename] [master]		( Downloads bookmark history and incorporates changes )


----------------------------------------------------------------------------------------------------------------------------------------
