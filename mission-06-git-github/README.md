# Mission 6 - Git and GitHub

## 1. Task / objective
The objective of this mission was to understand the core Git staging and commit workflow, create a separate feature branch (`update-about`), update the root `README.md`, publish the branch to GitHub to open a Pull Request, and build a concise glossary of essential Git commands.

## 2. Work completed

### Task 6.1 - Understand the basic Git workflow
| Git operation | What it does in your own words |
| :--- | :--- |
| Check repository status | Inspects the working directory and staging area to show which files are modified, untracked, or ready to be committed (`git status`). |
| Stage selected changes | Adds specific modified or new files into the staging area (index) so they are queued for the next snapshot (`git add <file>`). |
| Create a commit | Saves a permanent, timestamped snapshot of all staged changes into the local repository's history with a descriptive message (`git commit -m "..."`). |
| View commit history | Displays a chronological log of past commits along with their commit hashes, authors, dates, and messages (`git log`). |

- **Difference between staging and committing:** Staging (`git add`) acts as a preparation step where you selectively choose which file changes belong together in the next update, allowing you to review or adjust them before finalizing. Committing (`git commit`) permanently records those staged changes as a distinct version checkpoint in the project's history.

### Task 6.2 & 6.3 - Branching and Pull Request workflow
- Created and switched to a new branch named `update-about` from `main`.
- Added a `## My Learning` section to the root `README.md` summarizing key takeaways from previous missions, committed the change, and pushed `update-about` to GitHub.
- Opened a Pull Request on GitHub comparing `update-about` into `main` with a summary of the changes.
- **Pull Request Status:** **Merged** into `main` on GitHub (visible under the Closed Pull Requests tab, and the merged changes have been pulled back into the local `main` branch).
- **Why branches and Pull Requests are useful:** A branch creates an isolated workspace so developers can build new features or test edits without breaking the stable `main` codebase. A Pull Request provides a structured review step where teammates can inspect line-by-line diffs, discuss improvements, and verify changes before merging them into `main`.

### Task 6.4 - Git command glossary
| Git operation | Command | One-line explanation |
| :--- | :--- | :--- |
| Initialise a repository | `git init` | Creates a new hidden `.git` directory to start tracking a local project folder with Git version control. |
| Check status | `git status` | Displays the current branch name alongside any untracked, modified, or staged files. |
| Stage changes | `git add <file>` | Moves specific file modifications from the working directory into the staging area for the next commit. |
| Commit changes | `git commit -m "msg"` | Records a permanent snapshot of the currently staged changes in the local repository history. |
| View history | `git log` | Lists previous commits in reverse chronological order with commit IDs, authors, timestamps, and messages. |
| Create or list branches | `git branch` | Lists all existing local branches or creates a new branch pointer when given a branch name. |
| Switch branches | `git checkout <branch>` | Switches the active working directory to another branch (or creates and switches with `-b`). |
| Publish changes | `git push` | Uploads local branch commits to the remote repository on GitHub. |
| Retrieve remote changes | `git pull` | Fetches the latest commits from a remote branch on GitHub and merges them into the active local branch. |

## 3. Commands / tools used
- `git status` and `git log`: Inspected working tree state and verified commit history.
- `git checkout -b update-about`: Created and switched to the new feature branch.
- `git add`, `git commit`, and `git push -u origin update-about`: Staged, committed, and published the branch changes to GitHub.
- `git checkout main` and `git pull origin main`: Switched back to `main` and pulled the merged Pull Request changes locally.
- **VS Code** & **GitHub Web Interface**: Edited Markdown files locally and created/reviewed the Pull Request online.

## 4. My understanding
I understood how Git separates editing, staging, and committing to give developers fine-grained control over version history. Practicing with branches and Pull Requests showed how teams collaborate safely on the same repository without overwriting or destabilizing production files on `main`.

## 5. Difficulties faced
When first pushing the newly created `update-about` branch, running a plain `git push` returned an error because the local branch did not yet have a matching upstream branch configured on GitHub.

## 6. How I resolved them
I used `git push -u origin update-about` to set the remote tracking upstream branch on the first push, which published the branch cleanly and enabled the Pull Request prompt on GitHub.

## 7. Evidence / files
- `mission-06-git-github/README.md` (Workflow analysis, PR documentation, and Git command glossary).
- Root `README.md` (Updated with the `My Learning` section via the `update-about` branch and merged into `main`).

## 8. Commit details
- **Commit message:** `Complete Git and GitHub collaboration mission`
- **Status:** Committed and pushed to GitHub (`main` branch), with branch `update-about` and its merged Pull Request visible in the repository's PR history.