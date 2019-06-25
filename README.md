######GIT COMMANDS

[Visual Git Cheat Sheet ](http://ndpsoftware.com/git-cheatsheet.html#loc=stash;)

[Git Documentation](https://git-scm.com/docs)

[Setting up a repository help tutorial](https://www.atlassian.com/git/tutorials/setting-up-a-repository)


----------------------------------------------------------------------------------------------------------------------------------------
### CONFIGURE TOOLING
Configure user information for all local repositories

- git --version						                                           ( Check Version )

- git config --global user.name "[name]"                             ( Sets the name you want atached to your commit transactions )

- git config --global user.email "[email address]"                   ( Sets the email you want atached to your commit transactions )

- git config user.email					                                     ( Show email )

- git config user.name                                               ( Show username )

- git config --global color.ui auto                                  ( Enables helpful colorization of command line output )

- git config --list					                                         ( List of all Config )

- git remote								( Shows info about the remote repo )

- git remote add [RemoteRepoName] [Github Repo adress]			( Add a remote repository ) 

- git help [Command]					              	 ( Show help for the command )


----------------------------------------------------------------------------------------------------------------------------------------
### Create Repositories
Start a new repository or obtain one from an existing URL

- $ git init [project-name]					( Creates a new local repository with the specified name )

- $ git clone [url]          ( Downloads a project and its entire version history )


----------------------------------------------------------------------------------------------------------------------------------------
### Make Changes
Review edits and craf a commit transaction

- git status  ( Lists all new or modified files to be commited )

- git diff   ( Shows file differences not yet staged )

- git add . // git --all    ( Add all the changes )

  - git add *.txt     ( Add all txt files in current directory )

  - git add *.html    ( Add all html files in current directory )

  - git add [File]  ( Snapshots the file in preparation for versioning )
  
- git diff --staged   ( Shows file differences between staging and the last file version )

- git reset [File]    ( Unstages the file, but preserve its contents )

- git commit -m "[descriptive message]"   ( Records file snapshots permanently in version history )

- git commit -am "MESSAGE" // git commit -a -m "MESSAGE"	( Adds changes and Commit in same time )

- git commit --amend -m "MESSAGE"				( Change the last commit )


----------------------------------------------------------------------------------------------------------------------------------------
### Group Changes
Name a series of commits and combine completed efforts

- git branch					( Lists all local branches in the current repository )

- git branch [Branch-name]			          ( Creates a new branch )

- git checkout [Branch-name]           	( Switches to the specified branch and updates the working directory )

- git merge [Branch]	              ( Combines the specified branch’s history into the current branch )

- git branch -d [branch-name]			        ( Deletes the specified branch )


----------------------------------------------------------------------------------------------------------------------------------------
### Refactor Filenames
Relocate and remove versioned files

- git rm [file]					( Deletes the file from the working directory and stages the deletion )

- git rm --cached [file]			( Removes the file from version control but preserves the file locally )

- git mv [file-original][file-renamed]		( Changes the file name and prepares it for commit )


----------------------------------------------------------------------------------------------------------------------------------------
### Review History
Browse and ispect the evolution of project files

- git log					( Lists version history for the current branch, Check what branch you are currently on )

- git log --follow [file]			( Lists version history for a file, including renames )

- git log --author="[User]"			( Lists commit from specific user )

- git show HEAD					( Show the most recently commit HEAD )

- git diff [first-branch]...[second-branch]	( Shows content differences between two branches )

- git show [commit]				( Outputs metadata and content changes of the specified commit )


----------------------------------------------------------------------------------------------------------------------------------------
### Redo Commits
Erase mistakes and craft replacement history

- git reset [commit]				( Undoes all commits after [commit], preserving changes locally )

  - git reset --hard [commit]			( Discard all history and changes back to the specified commit )

  - git reset HEAD [Filename]			( Remove file from staging area )

  - git reset --hard HEAD^			( Undo last commit, and all changes )

  - git reset --hard HEAD^^			( Undo last 2 commits, and all changes )

  - git reset --soft HEAD^			( Undo last commit, put changes into stagin )


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

- git fetch [bookmark]				( Downloads all history from the repository bookmark )

- git merge [bookmark]/[branch]			( Combines bookmark`s branch into current local branch )

- git push [alias][branch]			( Uploads all local branch commits to GitHub )

- git pull [ Remotename ] [master]		( Downloads bookmark history and incorporates changes )


----------------------------------------------------------------------------------------------------------------------------------------
