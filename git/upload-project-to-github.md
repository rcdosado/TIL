# Upload project to github

TIL how to add repo from local to github (but not really just today)

This TIL assumes you have a local git repo on your computer

A. create a new repo in your github (select gitignore and license or not)
B. copy the link (one that ends in .git) from your repo
C. go to the root of your local repo
then type:
	```Bash
	
	git remote add origin <link> 
	git pull <link>
	git push
	```

D. this will ask you for your account values, then it will sync your local repo to your github repo

1. the command lets you point the destination repo, when you exec. push command
2. the command lets you merge the newly created repo from github to your local repo, no need to commit.
3. the command simply says "go ahead and sync current repo to the origin repo" since origin points to the github repo, then that is the destination.

thats it.




