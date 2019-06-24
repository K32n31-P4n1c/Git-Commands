### Git Commands

git --version						( Version )

git config --global user.name "USERNAME"		( Create Username )

git config user.name					( Show Username )

git config --global user.email "EMAIL"			( Create E-mail )

git config user.email					( Show email )

git config --list					( List of all Config )

git help COMMAND					( Show help for the command )

--------------------------------------------------------------------------------------------------------------------------------

git init						( Initialize git repository )

git remote add REMOTEREPONAME GITHUB_REPO_ADDRES		( Add a remote repository ) 

git remote 						( Shows information  about the Remoterepo )

git remote 						( Shows remote repo )



git push -u REMOTEREPONAME master			( Push changes from remoterepo to githubproject )

git pull REMOTEREPONAME master				( Pull changes from github to remoterepo )

git clone                             ( Clone Repository Into a New Directory )


# git add .	// 	git --all			( Add all the changes )
- git add FILENAME					( Add specific change )
- git add *.txt						( Add all txt files in current directory )
- git add *.html          ( Add all html files in current directory )


git diff						( Show unstaged differences since last commit )

git diff --staged					( Show stagged differences )


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

git status						( View Changes )

git log							( View commit history )

git show HEAD						( Show the most recently commit HEAD )

git log --author="USER"					( View commit from specific user )

git rm FILENAME						( Delete some file )

git rm --cached FILENAME      ( Delete file, delete file from stagged area )
