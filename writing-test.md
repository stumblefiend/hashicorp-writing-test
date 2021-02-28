## Learn the difference between push, pull, and fetch

- `git push` - sends changes from a local branch to a remote repo
- `git fetch` - gets changes from a remote repo into your tracking branch
- `git pull` - gets changes from a remote branch into your tracking branch and merges them into a local branch

`git push` and `git pull` are often described as equivalent. However, `git pull` performs a `git fetch` then a `git merge`. Some people prefer to use `git fetch` followed by `git merge` to ensure they first understand the changes before merging them into their branch.

`git push` checks if your current branch is connected to a tracking branch for a remote repository. If so, git pushes changes from your branch to the remote branch. This is how code is shared with a remote repository. `git push` makes the remote branch resemble your local branch. This fails if the remote branch diverges from your local branch. If not all the remote branch commits are in your local branch, synchronize your local branch with the remote branch via `git pull` or `git fetch` and `git merge`.

`git fetch` checks if your current branch is connected to a tracking branch before pulling changes into the tracking branch. `git fetch` does not change your local branch unless you use `git merge origin/master` (for the "master" branch) to merge those changes into your branch - probably also called "master". 
