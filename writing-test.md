## What is the difference between push, pull, and fetch?

- `git push` - sends changes from a local branch to a remote repo
- `git fetch` - gets changes from a remote repo into your tracking branch
- `git pull` - gets changes from a remote branch into your tracking branch and merges them into a local branch

`git push` and `git pull` are often described as equivalent. However, `git pull` does two things. `git pull` simply does a `git fetch` followed by `git merge`. This is often the desired result, but some people prefer to use `git fetch` followed by `git merge` to ensure they first understand the changes before merging them into their branch.

`git push` takes your current branch, and checks for a connected tracking branch for a remote repository. If so, git pushes changes from your branch to the remote branch. This is how code is shared with a remote repository. You can think of it as "make the remote branch resemble my local branch." This fails if the remote branch diverges from your local branch. If not all the remote branch commits are in your local branch, synchronize your local branch with the remote branch via `git pull` or `git fetch` and `git merge`.
 
`git fetch` again takes your current branch, and checks to see if there is a tracking branch. If so, it looks for changes in the remote branch, and pulls them into the tracking branch. It does not change your local branch. To do that, use `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master". 
