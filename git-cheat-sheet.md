# Git Cheat Sheet

* * *

## Basic Commands

| Command | Description |
| --- | --- |
| `git init` | Initialize a new Git repository |
| `git clone <url>` | Create a local copy of a remote repository |
| `git add <file>` | Stage changes to a specific file |
| `git add .` | Stage all changes in the current directory |
| `git commit -m "<message>"` | Commit staged changes |
| `git status` | Check the status of changes |
| `git log` | View the commit history |
| `git push` | Push local commits to the remote repository |
| `git pull` | Fetch and merge changes from the remote |

* * *

## Branching & Merging | Remote Repositories

| Command | Description |
| --- | --- |
| `git branch` | List all branches |
| `git remote -v` | List all remote repositories |
| `git branch <name>` | Create a new branch |
| `git checkout <name>` | Switch to a different branch |
| `git merge <name>` | Merge the specified branch into the current branch |
| `git branch -d <name>` | Delete a branch |

* * *

## Undoing Changes | Pushing Changes

| Command | Description |
| --- | --- |
| `git reset <file>` | Unstage changes to a specific file |
| `git reset --hard HEAD` | Discard all uncommitted changes in the working directory |
| `git revert <commit_hash>` | Create a new commit that undoes the changes made in a previous commit |

- **Why force push?**
    - To overwrite remote history after rebasing or squashing commits.
    - **Caution:** Can cause data loss for others if they've based work on the overwritten commits.

* * *

## Squashing Commits

- **Why squash?** Combine multiple commits into one, creating a cleaner commit history.
- **How:**
    1. `git rebase -i HEAD~<number_of_commits>` (replace `<number_of_commits>` with the desired number)
    2. An editor will open. Change `pick` to `squash` for commits you want to combine, leaving the first one as `pick`.
    3. Save and close the editor. A new editor will open to edit the combined commit message.
    4. Save and close to complete the squash.

* * *

## 🎁 Additional Tips

- Use clear and descriptive commit messages.
- Pull changes frequently to avoid conflicts.
- Create branches for new features or bug fixes.
- Use `git log` to track changes and understand the project history.
- Tag work in progress by prefixing the commit message with //WIP:
- For premade .gitignore files check out the repo on GitHub [https://github.com/github/gitignore](https://github.com/github/gitignore)
- Explore online resources and tutorials to learn more about Git!

* * *

GitHub Cheat Sheet v1.0 by Goran Tomasic - **[www.digiden.dev](http://www.digiden.dev)**
