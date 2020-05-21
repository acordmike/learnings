Swash commits and rebase
* Update the remote branch
`git pull origin master`

* Squash all commits made after branching
Run following to see log commit log history 
`git log --graph --decorate --pretty=oneline --abbrev-commit`

Grab the SHA1 of the first branched commit.

Run the following to swash to that commit:
``git rebase -i [SHA]``

Finally, rebase onto remote branch
`git rebase master`
