## Tutorial Git



### Create new folder

````
git init 
git add . or git add <filename>
git commit -m "<message>"
git push origin master or git push origin -u master 
````

### Create new remote

````
git remote add origin <linkofgitremote>
git remote -v
	
````

### Git Branching

````
git branch // show branch
git checkout -b <newbranch> // create branch
git checkout <master or branch>
````



### Git Merge & Diff

````
git diff // only compare it with previous one
git diff <namabranch> // it means compare current brnch/master to namabranch
git merge <namabranch|master> //it means you will merge <namabranch|master> to current  								branch


````



### Undoing Commit

````
git reset HEAD~1  // back to stage one
git reset --hard HEAD~1 //complete rollback to previous one
````

### Git logs

````
git log
git log --oneline

````
### REBASE BRANCH TO MASTE
````


git checkout feature
git rebase main


````
### Specific file to change to previous one

````
git show 6f5ea:testdata/data.txt 
git checkout 6f5ea testdata/data.txt
git commit -m "uncheckone"
git status

````

