###### GIT COMMANDS

----------------------------------------------------------------------------------------------------------------------------------------
### CONFIGURE TOOLING
Configure user information for all local repositories

- git --version						                                           ( Version )

- git config --global user.name "[name]"                             ( Sets the name you want atached to your commit transactions )

- git config --global user.email "[email address]"                   ( Sets the email you want atached to your commit transactions )

- git config user.email					                                     ( Show email )

- git config user.name                                               ( Show username )

- git config --global color.ui auto                                  ( Enables helpful colorization of command line output )

- git config --list					                                         ( List of all Config )

- git help [Command]					                                       ( Show help for the command )

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

----------------------------------------------------------------------------------------------------------------------------------------

git remote add REMOTEREPONAME GITHUB_REPO_ADDRES		( Add a remote repository ) 

git remote 						( Shows information  about the Remoterepo )

git remote 						( Shows remote repo )



git push -u REMOTEREPONAME master			( Push changes from remoterepo to githubproject )

git pull REMOTEREPONAME master				( Pull changes from github to remoterepo )




					( Show stagged differences )


git commit -m "MESSAGE"					( Commit the changes )

git commit -am "MESSAGE" // git commit -a -m "MESSAGE"	( Adds changes and Commit in same time )


git branch						( Check what branch you are currently on )

git branch BRANCHNAME					( Create new branch )

git checkout BRANCHNAME					( Switch to branch )

GIT branch -d BRANCHNAME				( Delete branch name )


git checkout HEAD FILENAME				( Discards changes in the working directory. )

git reset HEAD FILENAME					( Remove file from staging area )

git reset --soft HEAD^					( Undo last commit, put changes into stagin )

git reset --hard HEAD^					( Undo last commit, and all changes )

git reset --hard HEAD^^					( Undo last 2 commits, and all changes )

git commit --amend -m "MESSAGE"				( Change the last commit )

git checkout -- FILENAME				( Blow away all changes since last commit )
git reset SHA						( RCan be used to reset to a previous commit in your commit history., need jst frst 7digits )


git log							( View commit history )

git show HEAD						( Show the most recently commit HEAD )

git log --author="USER"					( View commit from specific user )

git rm FILENAME						( Delete some file )

git rm --cached FILENAME      ( Delete file, delete file from stagged area )


----------------------------------------------------------------------------------------------------------------------------------------
### Group Changes
Name a series of commits and combine completed efforts
