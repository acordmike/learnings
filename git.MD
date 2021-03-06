Swash commits and rebase
* Update the remote branch
`git checkout master`
`git pull`
`git checkout feature/branchname`

* Squash all commits made after branching
Run following to see log commit log history 
`git log --graph --decorate --pretty=oneline --abbrev-commit`

Grab the SHA1 of the last commit before branching.

Run the following to swash to that commit:
``git rebase -i [SHA]``

Change all commits from *pick* to *squash* except the last one (top one) and save file

Remove all intermediate comments and create one overall comment and save file

Finally, rebase onto remote branch
`git rebase master`
