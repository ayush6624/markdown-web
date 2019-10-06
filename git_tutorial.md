# Git Tutorial

# GPG verification : 
> git config commit.gpgsign true

___
## Initialise git in a folder : 
>git init

## download a repo : 
> git clone `<URL>`  


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
> git remote prune origin      (To clean stale branches)

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

## Interactive Rebase
* **Dont forget** to do `git push -f`
* git rebase -i HEAD~5
* (Replace 5 with the number of commits, no harm in putting a higher number)
* They are from Older to Newer
* `pick` for the ones you want to stay
* `squash` for the on which you want to `squash` to the upper one. Remember that do not put `sqaush` on the topmost one. Multiple sqashes would be squashed to the `pick` commit in bottom to up direction.
* After `sqashing`, comment out the original commit message(s) and put your own one and Voila, it's done!
* To keep the commit message of the commit which you are squashing into, use `fixup` or `f` (For the lazy guys like me :P)
* To delete use `drop` or `d` to delete them from commit history, *Remember* your work on the commit will be lost
* Rewording can also be done by using `r`
* `Reordering` can be done by just reorering with the `pick` prefix
* Any time you feel that you have messed up, do a `git rebase --abort`, and to continue use `git rebase --continue
* You can use single letters to get it done

## Stashing
- Suppose You are working on a feature, and you realise that you were working on the master branch, so simply do `git stash` to save the local changes
- You can also do this in case something else comes to your mind.
- Remember you can always view your stash from `git stash --list`
- To apply the stash, do `git stash apply`

## Misc
- Merge the staged things to the last commit : `git commit --amend --no-edit`
## Rebasing technique:
* *Make a new branch from master -* `feature`
* `git checkout feature`
* `<DO THE CHANGES>`
* `git rebase master`
* `git checkout master`
* `git merge feature`

In *GitKraken*
* Do appropriate 


This would be a clean commit tree

git reset -- HEAD^ >>> ^ for number of undo
--soft --hard flags also