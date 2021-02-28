## Learn the difference between push, pull, and fetch

- `git push` - sends changes from a local branch to a remote repo
- `git fetch` - gets changes from a remote repo into your tracking branch
- `git pull` - gets changes from a remote branch into your tracking branch and merges them into a local branch

`git push` first checks whether your current branch is connected to a tracking branch for a remote repository. Then, it makes the remote branch resemble your local branch. A `git push` fails if the remote branch diverges from your local branch. To resolve the issue, synchronize your local and remote branch via `git pull` or `git fetch` and `git merge`.

`git push` and `git pull` are often described as equivalent. However, `git pull` performs a `git fetch` then a `git merge`. Some people prefer `git fetch` in order to first review changes before merging branches.

`git fetch` checks whether your current branch is connected to a tracking branch before pulling changes into the tracking branch. `git fetch` does not change your local branch unless you use `git merge origin/master` to merge changes into your branch called "master." 


