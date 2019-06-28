# Git Tutorial

## Initialise git in a folder : 
>git init

## download a repo : 
> git clone `<URL>`  

## GPG verification : 
> git config commit.gpgsign true

## See list of branches : 
> git branches   *(git branches -r for listing remote branches)*
## Checking the status of git repo :
> git status
## Make a commit :
>git add * && git commit -m "COMMIT_MESSAGE"  

`Stage them all and write the COMMIT_MESSAGE and do Ctrl + Enter`  

## Logging in Git : 
> git log (--oneline)  

## Making a new branch and checking it out :
> git checkout -b branch_name
## Deleting a branch locally :
>  git branch -d branch_name (-D for force)

## Deleting a branch remotely : 
> git push origin :branch_name
## Update a branch from remote (Local is behind remote) :
> git pull
## Push changes in a branch to remote : 
>git push `(git push origin master)`

---

## Best Practice 
* Branch often!
* For every new feature you are unsure of
* commit is not a single file change rather, an action, so you can have multiple files added/deleted under a single commit with an appropritate message
* `Use GitKraken`

---

## Rebasing technique:
* *Make a new branch from master -* `feature`
* `git checkout feature`
* `<DO THE CHANGES>`
* `git merge master`
* `git checkout master`
* `git merge feature`

In *GitKraken*
* Do appropriate 


This would be a clean commit tree

git reset -- HEAD^ >>> ^ for number of undo
--soft --hard flags also