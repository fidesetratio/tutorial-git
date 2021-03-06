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

### change branch to master
````
git checkout <branch_name>
git merge --strategy=ours master    # keep the content of this branch, but record a merge
git checkout master
git merge <branch_name>            # fast-forward master up to the merge
git push origin master
````


### getting all changes one and compare it manually per branch
```
			-          + 
git diff --name-only development..master 
or
git diff --name-only development..HEAD

git diff --name-only -z --diff-filter=ACMRT development..HEAD | xargs -0 git archive -o update.tar.gz HEAD --
git diff --name-only -z --diff-filter=ACMRT HEAD..development | xargs -0 git archive -o update-dev.tar.gz development --

beda nya development..master
- artinya dari development
+ artinya itu dari master

```
### tips and trick jika ngak ada tools untuk lihat hasil perubahan
```
			-          + 
git diff --name-only development..master
git diff --name-only development..HEAD


git diff --name-only -z --diff-filter=ACMRT  origin/testbranch..origin/master | xargs -0 git archive -o update.tar.gz origin/master --
git diff --name-only -z --diff-filter=ACMRT  origin/master..origin/testbranch | xargs -0 git archive -o update-dev.tar.gz origin/testbranch --


beda nya development..master
- artinya dari development
+ artinya itu dari master

git diff  development..master -- src/main/java/com/app/controller/AdMedikaController.java




git remote add temp https://github.com/fidesetratio/problemku
git remote -v
git push temp namabranch
			-          + 

Note : gunakan public git repository

			
			
```
### Git memaksa agar mereplace content branch atau master dengan new one
```
 git push -f origin master
  or
 git push -f origin <nama_branch> 
```


### Git log commit agar bagus
```
 git config --global alias.lol "log --graph --decorate --pretty=oneline --abbrev-commit --all"
 git lol
```
### Git untuk stash
```
Stash

 git stash save "Message"
 git stash list
 git stash apply stash@{0} => ini dilakukan jika emang tidak perlu delete stash dari list
 git stash pop ==>  ini di lakukan jika ingin mau ambil stash yang terakhir
 git stash drop stash@{1} ==> delete stash
 git stash clear ==> delete all stsash
 git stash branch my-branch ==> tolong apply stash branch ke new branch my-branch
 git stash show stash@{2} ==> Please use this to show stash detail
 git stash -u ==> ini untuk menstash semua data yang belum di commit kecuali .gitignore
 git stash -all ==> ini untuk menstash semua data yang belum di commit 
 
```
