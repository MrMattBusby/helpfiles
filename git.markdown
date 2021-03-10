# Repos
### Cloning
- `git clone <link>`
### Creating
- `git init <repo-name>` _makes .git folder_

# Branching
### Creating
- `git branch <branch-name>` _created locally_
> `git push -u <remote> <branch-name>` _push to remote repo_
### Viewing
- `git branch #--list`
### Merging
> Switch to branch, update local dev, merge your features into dev
- `git checkout <dev> ; git fetch ; git merge <branch-name>`

# Local
### Checking out
> To checkout, your current branch must be committed/stashed
- `git checkout <branch-name>`
- `git checkout -b <branch-name>` _create and checkout_
### Status
> Staged files are in **green** after an `add`
- `git status`
### Add
- `git add <file>`
- `git add -A` _all_
### Unstage
- `git reset <file|hash>` _unstages without editing file_
### Reverting
- `git revert <hash>` _created another commit, not deleting your prev_
### Diff
- `git diff` _unstaged_
- `git diff -staged`
- `git diff <branch1> <branch2>`
### Log
- `git log` _-follow[file] to follow file renames_
### Committing, tagging
- `git commit -m "message"` _locally_
- `git tag -a <version> -m <message> <hash>` _readable version/desc_
### Stash
- `git stash save "message"` _store_
- `git stash pop` _recall_
- `git stash list` _list all, or `show` for changes_

# Remote
### Pushing
- `git push <remote> <branch-name>` _if new branch: --set-upstream_
> or
- `git push -u origin <branch-name>`
### Pulling
- `git pull <remote>` _combo of fetch and merge_


