## Comparing git push, pull, and fetch

- `git push` - Sends changes from a local branch to a remote repository.
- `git fetch` - Gets changes from a remote repository into your tracking branch.
- `git pull` - Gets changes from a remote branch into your tracking branch and merges them into a local branch.

Both `git push` and `git fetch` first check whether your current branch is connected to a tracking branch for a remote repository before proceeding. A `git push` fails if the remote branch diverges from your local branch. Synchronize your local and remote branch via `git pull` or `git fetch` and `git merge` to resolve the issue.

`git fetch` allows you to review changes before merging branches. `git fetch` only changes your local branch when you use `git merge`. For example, `git merge origin/master` merges changes into your local branch called "master." `git fetch` and `git pull` are often described as equivalent. However, `git pull` performs a `git fetch` then a `git merge`.

