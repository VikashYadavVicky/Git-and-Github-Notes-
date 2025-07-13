# Git and GitHub

## 🔹 What is Git?

**Git** is a **distributed version control system** used to track changes in source code during software development.  
It allows multiple developers to work on a project simultaneously without interfering with each other’s work.

### ✅ Key Features of Git:
- Tracks code history and changes.
- Supports branching and merging.
- Works offline (locally).
- Fast and efficient.

---

## 🔹 What is GitHub?

**GitHub** is a **cloud-based platform** that hosts Git repositories.  
It provides a graphical interface and collaboration tools like issues, pull requests, and wikis.

### ✅ Key Features of GitHub:
- Hosts Git repositories online.
- Helps developers collaborate on code.
- Offers tools like pull requests, issue tracking, and GitHub Actions.
- Provides GUI-based version control through web.

---

## 🔄 Summary: Git vs GitHub

| Feature         | Git                          | GitHub                          |
|-----------------|------------------------------|----------------------------------|
| Type            | Version Control System       | Hosting Platform for Git        |
| Works Offline   | ✅ Yes                        | ❌ No (requires internet)        |
| Interface       | Command Line (CLI)           | Graphical (Web UI)              |
| Purpose         | Manage code locally          | Share & collaborate on code     |

---

🔸 End of Page 1 🔸

---

## 🔹 Common Terminal Commands (with Examples)

**1. Change directory:**  
cd <folder_name>  
👉 Example: `cd my_project`

**2. Go back one directory level:**  
cd ..  
👉 Example: from `/home/user/project` to `/home/user`

**3. Create a new directory:**  
mkdir <folder_name>  
👉 Example: `mkdir notes`

**4. List all files Using ls (including hidden :- ls -ls):**  
ls
👉 Example: `ls`
ls -la  
👉 Example: `ls -la`

**5. Clear terminal screen:**  
clear  
👉 Example: `clear`

**6. Print current working directory:**  
pwd  
👉 Example: `pwd`  
🧾 Output: `/home/user/my_project`

**7. Create a new empty file:**  
touch <filename>  
👉 Example: `touch index.html`

**8. Rename a file or folder:**  
mv <old_name> <new_name>  
👉 Example: `mv old.txt new.txt`

**9. Move a file to a folder:**  
mv <file> <folder>  
👉 Example: `mv notes.txt my_folder/`

**10. Copy a file:**  
cp <source> <destination>  
👉 Example: `cp file1.txt backup/`

**11. Delete a file:**  
rm <filename>  
👉 Example: `rm old_file.txt`

**12. Delete a folder and its contents:**  
rm -r <folder_name>  
👉 Example: `rm -r old_folder`

**13. View the content of a file:**  
cat <filename>  
👉 Example: `cat readme.md`

**14. Edit file using nano editor:**  
nano <filename>  
👉 Example: `nano notes.txt`  
➡️ To save `Ctrl+O `and exit: `Ctrl + X`, then press `Y`, then `Enter`


## 🔹 What is `echo` in Terminal?

The `echo` command is used to **display a line of text** or **write text into a file** in the terminal.

### ✅ Use Cases:

**1. Print a message on the terminal:**

echo "Hello World"  
🧾 Output:  
Hello World

**2. Create a new file with some content:**

echo "This is a test file." > test.txt  
👉 Creates a file `test.txt` with the content:  
This is a test file.

**3. Append content to an existing file:**

echo "Another line." >> test.txt  
👉 Adds the line `"Another line."` to the end of `test.txt` without deleting the existing content.

### 📌 Notes:
- Use `>` to **create/overwrite** a file.
- Use `>>` to **append** to a file.

---

🔸 End of Page 2 🔸

---

# Git Commands

### 🔹 To create user (Global)

git config --global user.name "your_name"  
git config --global user.email "your_email@example.com"

➡️ For specific repository, just remove `--global`.


### 🔹 To clone a GitHub repository
git clone <repository_link>

### 🔹 Adding and Committing Files

**Add file to staging area:**  
git add <filename>  
👉 Example: git add file1.txt

**Commit staged changes with a message:**  
git commit -m "some meaningful comment"  
👉 Example: git commit -m "Added file1.txt"

### 🔹 Git Workflow Stages
**Working Directory → Staging Area → Local Git Repo**

file1.txt  
  │  
  └──> git add  
     │  
     └──> file1.txt (staged)  
        │  
        └──> git commit  
            ↓  
          Saved to Git folder
          
### 🔹 Check Status of Files
**Check current status of all files:**  
git status

### 🔹 Commit and Add Tracked Files in One Command
git commit -a -m "message"  
👉 This adds and commits all **already tracked files** in one command.  
⚠️ Does not include new/untracked files.

### 🔹 Add All Files at Once
git add .  
👉 Adds all files (new and changed) in the current folder.

### 🔹 Push Changes to Remote
git push  
👉 Uploads all commits from local repo to remote (e.g., GitHub).

### 🔹 Pull Latest Changes from Remote
git pull  
👉 Downloads the latest changes from the remote repo into your local repo.

### 🔹 List All Files (Including Hidden)
ls -a  
👉 Shows all files, including hidden ones like `.git`.

### 🔹 View Git Commit History

**Basic log:**  
git log

**Detailed log with code diffs:**  
git log -p

**Show only last 2 commits:**  
git log -2

---

🔸 End of Page 3 🔸

---

## 🔹 Push Local Repo to GitHub

### Step-by-step process:

1. **Create a folder using `mkdir`:**

mkdir <reponame>

2. **Move into that directory:**

cd <reponame>

3. **Initialize Git repo:**

git init

4. **Create any file (example):**

echo "# My Project" > readme.md

5. **Add file(s):**

git add .

6. **Commit files:**

git commit -m "initial commit"

---

### On the other side (GitHub):

- Create a new GitHub repository  
- ❌ Do NOT add a README file  
- Then copy the remote repo URL


---

### 🔹 Connect Local Repo to GitHub (New Steps)
**Change branch name from master to main:**  
git branch -M main

**Add remote repository:**  
git remote add origin <url>

**Push local branch to remote:**  
git push -u origin main

---

# 🌿 Branching in Git

## 🔹 Check Existing Branches

**List all local branches:**  
`git branch`  
➡️ Shows all branches available locally.  

---

## 🔹 Create a New Branch

**Create a branch without switching to it:**  
`git branch <branchname>`  
➡️ Creates a new branch from the current HEAD.

---

## 🔹 Switch to a Branch

**Switch to an existing branch (old method):**  
`git checkout <branchname>`

**Switch using the modern command:**  
`git switch <branchname>`  
➡️ Recommended for readability and clarity.

---

## 🔹 Create and Switch in One Command

**Create a branch and switch to it immediately:**  
`git checkout -b <branchname>`  
or  
`git switch -c <branchname>`

---

## 🔹 Merge a Branch

**Merge a branch into the current branch:**  
`git merge <branchname>`  
➡️ Brings the target branch’s changes into your current branch.

---

## 🔹 Apply a Specific Commit from Another Branch

**Cherry-pick a commit into your current branch:**  
`git cherry-pick <commit-hash>`  
➡️ Applies the changes from the selected commit.

---

## 🔹 Show Merged and Unmerged Branches

**Show branches already merged into current branch:**  
`git branch --merged`

**Show branches not yet merged into current branch:**  
`git branch --no-merged`

---
## 🔹 Delete a Branch

**Delete a local branch after it’s merged:**  
`git branch -d <branchname>`  
➡️ Safe delete; only removes if already merged.

---

**Force delete a local branch (even if not merged):**  
`git branch -D <branchname>`  
➡️ Use with caution—this does not check for unmerged changes.

---

---

🔸 End of Page 3 🔸

---

# Git Concepts

## 🔹 What is `HEAD` and `head`?

In simple terms, if you're working in the `main` branch, that branch is your active branch.  
So, `HEAD` points to the current **main** branch (or any other active branch you're on).

And head is the others branch. Means Head point main current branch or active branch the head 
Point rest of all branches

If you switch to another branch, `HEAD` will now point to that new active branch.

📝 Basically:  
**HEAD = a reference that points to the latest commit on your current (active) branch.**

This reference changes whenever you use `git checkout` or `git switch` to change branches.

> ✅ You can think of `HEAD` as Git’s way of saying:  
> “This is where you currently are — your working position in the repo.”

---

# 🔍 Git Show – One Page Cheat Sheet

## 🔹 View Commit Details

**Show latest commit on current branch:**  
`git show`  
➡️ Shows the latest commit with message, author, and code changes.

---

**Show Staged data:**  
`git show : <filename>`  
➡️ Show only staged data means those data they are add but not commit.

---

**Show a specific commit by hash:**  
`git show <commit_hash>`  
➡️ Displays details of that particular commit.

---

**Show commit in a short format:**  
`git show --oneline`  
➡️ One-line summary of the latest commit.

---

**Show commit without diff (message only):**  
`git show --no-patch`  
➡️ Hides code changes, shows commit metadata.

---

## 🔹 View File Content from Commits

**Show content of a file from latest commit:**  
`git show HEAD:<filename>`  
➡️ Displays the file content from the latest commit.

---

**Show content from previous commits:**  
  
➡️ Shows the file from the **third latest commit** (position 3 index 2).`git show HEAD~2:<filename>`
 
➡️ Shows the file from the **second latest commit** (position 2 index 1). `git show HEAD~1:<filename>` 
 
➡️ Also shows the file from the **second latest commit** (same as `HEAD~1`).`git show HEAD~:<filename>` 
  
➡️ Shows the file content from the **latest commit** (position 1 index 0)`git show HEAD:<filename>`
> 🧠 Tip: Use `HEAD~n` to access the file from the commit that is **n+1 positions back** from the current one.

---

**Show file from a specific commit:**  
`git show <commit_hash>:<filename>`  
➡️ Shows the file as it was in that commit.

---

## 🔹 See What Changed in Files

**Show only filenames changed in a commit:**  
`git show --name-only`  
➡️ Lists file names modified in the commit.

---

**Show files with type of changes (A/M/D):**  
`git show --name-status`  
➡️ A = Added, M = Modified, D = Deleted.

---

**Show commit stats (line changes per file):**  
`git show --stat`  
➡️ Quick summary of how many lines were added/removed.

---

**Show changes for a specific file in a commit:**  
`git show <commit_hash> -- <filename>`  
➡️ Isolate changes to just one file.

---

> 🧠 Tip: Use `git log` to find commit hashes for use with `git show`.

# 🔍 Git Diff – One Page Cheat Sheet

## 🔹 Compare Working Directory & Staging Area

**Compare unstaged changes (working directory vs last commit):**  
`git diff`  
➡️ Shows what you’ve modified but not yet staged.

---
---

**Show content from previous commits:**  
  
➡️ Shows the difference file from the **third latest commit** (position 3 index 2).`git diff HEAD~2 <filename>`
 
➡️ Shows the difference file from the **second latest commit** (position 2 index 1). `git diff HEAD~1 <filename>` 
 
➡️ Also shows the difference file from the **second latest commit** (same as `HEAD~1`).`git diff HEAD~ <filename>` 
  
➡️ Shows the difference file content from the **latest commit** (position 1 index 0)`git diff HEAD <filename>`
> 🧠 Tip: Use `HEAD~n` to access the file from the commit that is **n+1 positions back** from the current one.
> Use of ':' colon is optional for this

**Compare staged changes (index vs last commit):**  
`git diff --cached`  
or  
`git diff --staged`  
➡️ Shows changes that are staged and ready to commit.

---

**Compare both staged & unstaged changes:**  
`git diff HEAD`  
➡️ Compares working tree and index vs last commit.

---

## 🔹 Compare Specific Files

**Compare one file (unstaged):**  
`git diff <filename>`  
➡️ Shows changes made to that file (not staged).

---

**Compare one file (staged):**  
`git diff --cached <filename>`  
➡️ Shows staged changes for a specific file.

---

**Compare file with last committed version:**  
`git diff HEAD <filename>`  
➡️ Compare working file (staged + unstaged) vs last commit.

---

## 🔹 Compare Commits or Branches

**Compare two commits:**  
`git diff <commit1> <commit2>`  
➡️ Shows what changed from `commit1` to `commit2`.

---

**Compare branches:**  
`git diff <branch1>..<branch2>`  
➡️ Changes in `branch2` that are not in `branch1`.

---

**Compare with main branch:**  
`git diff main`  
➡️ Shows changes in current branch compared to `main`.

---

## 🔹 Output Customization

**Show only file names changed:**  
`git diff --name-only`  
➡️ Just lists file names that changed.

---

**Show file names with change type:**  
`git diff --name-status`  
➡️ A = Added, M = Modified, D = Deleted.

---

**Show word-level changes:**  
`git diff --word-diff`  
➡️ More granular view than line-based diff.

---

**Ignore whitespace differences:**  
`git diff -w`  
➡️ Hides changes that only involve whitespace.

---

> 🧠 Tip: Use `git log` + `git diff` together to inspect history and exact changes.

# 🔄 Git Reset – One Page Cheat Sheet

`git reset` is used to **undo commits or staging** by moving the HEAD pointer and optionally modifying the index and working directory.

---

## 🔹 Reset Types Overview

| Command                   | Affects Commit History | Affects Staging Area | Affects Working Directory |
|--------------------------|-------------------------|----------------------|----------------------------|
| `--soft`                 | ✅ Yes                  | ❌ No                | ❌ No                     |
| `--mixed` *(default)*    | ✅ Yes                  | ✅ Yes              | ❌ No                     |
| `--hard`                 | ✅ Yes                  | ✅ Yes              | ✅ Yes                    |

---

## 🔸 1. Undo Last Commit (Keep Changes)

```bash
git reset --soft HEAD~1
```
➡️ Removes the last commit but **keeps all changes staged**.  
Useful when you want to re-edit your commit or message.

---

## 🔸 2. Unstage Files (Keep Changes)

```bash
git reset HEAD <filename>
```
➡️ Unstages the file (removes from staging) but **keeps changes** in working directory.  
Same as `--mixed` but scoped to specific files.

---

## 🔸 3. Undo Last Commit and Unstage Changes

```bash
git reset --mixed HEAD~1
```
➡️ Removes the last commit and **unstages** the changes (moves them back to working directory).  
Default behavior of `git reset`.

---

## 🔸 4. Completely Undo Last Commit (Dangerous)

```bash
git reset --hard HEAD~1
```
➡️ Removes last commit **and discards all changes**.  
⚠️ Use with caution — changes are **permanently lost**.

---

## 🔸 5. Reset to Specific Commit

```bash
git reset --hard <commit-hash>
```
➡️ Resets your branch to a specific commit. Working directory and index will match that commit.

---

## 🔸 6. Reset Specific File to Last Commit

```bash
git reset --hard HEAD <filename>
```
➡️ Discards all local changes in the file and restores it to last committed state.

---

## 🔸 7. Dry Run (Preview)

```bash
git reset --mixed --dry-run HEAD~1
```
➡️ Previews what would be unstaged or reset — no actual changes made.

---

## 🔸 8. Reset Index (Unstage Everything)

```bash
git reset
```
➡️ Unstages all files (like `git reset --mixed HEAD`) — changes remain in working directory.

---
## 🔄 Unstage a File (Keep Changes in Working Directory)

git reset <filename>


## 🧠 Tip

Use `git log` to find commit hashes:  
```bash
git log --oneline
```

---

> ⚠️ Use `--hard` with extreme caution — once you run it, changes cannot be recovered unless committed or backed up.

# ♻️ Git Restore – One Page Cheat Sheet

`git restore` is used to **restore file content or unstage files**, introduced in Git 2.23 as a safer alternative to `git reset` and `git checkout`.

---

## 🔹 Unstage a File (Move from Staged to Unstaged)

```bash
git restore --staged <filename>
```

➡️ Removes the file from the staging area (index)  
but keeps the changes in your working directory.

---

## 🔹 Discard Local Changes (Restore from Last Commit)

```bash
git restore <filename>
```

➡️ Discards **uncommitted changes** and restores the file to the version in the last commit.

---

## 🔹 Restore from a Specific Commit

```bash
git restore -s <commit_hash or HEAD~n> <filename>
```

➡️ Replaces the file content with the version from the given commit.

**Example:**  
```bash
git restore -s HEAD~1 index.html
```
Restores `index.html` from **1 commit before HEAD**.

---

## 🔹 Restore Entire Directory or All Files

```bash
git restore .
```

➡️ Discards all uncommitted changes to all files in the directory.

---

## 🔹 Restore a Deleted File

If you've accidentally deleted a tracked file:

```bash
git restore <filename>
```

➡️ Recovers the file from the latest commit.

---

## 🧠 Tip:
Use `git log` to find commit hashes, then use `git restore -s <commit>` to bring files back from any point in history.

---

> ⚠️ Warning: `git restore` affects your working directory. Be sure you want to discard changes before using it without `--staged`.


# 🔁 Git Checkout in Git

## 🔹 Switch to an Existing Branch

**Switch to an existing branch (classic command):**  
`git checkout <branchname>`  
➡️ Changes your working directory to the specified branch.

---

## 🔹 Create and Switch to a New Branch

**Create and switch in one step:**  
`git checkout -b <branchname>`  
➡️ Creates a new branch and immediately switches to it.

---

## 🔹 Switch to a Remote Tracking Branch

**Track and switch to a remote branch:**  
`git checkout -b <local-branch> origin/<remote-branch>`  
➡️ Creates a local branch and links it to the remote branch.

---

## 🔹 Restore a File from Last Commit

**Restore a file to its last committed version:**  
`git checkout HEAD <filename>`  
➡️ Replaces current version of file with the one from HEAD.

---

## 🔹 Restore a File from a Specific Commit

**Bring back a file from a previous commit:**  
`git checkout <commit-hash> -- <filename>`  
➡️ Restores the file content from the selected commit.

---

## 🔹 Checkout a Specific Commit (Detached HEAD)

**View an older commit (detached state):**  
`git checkout <commit-hash>`  
➡️ Puts you in a detached HEAD state.  
Use `git checkout -b <branchname>` to save your changes on a new branch.

---

## 🔹 Restore a Deleted File from History

**Recover a deleted file from a past commit:**  
`git checkout <commit-hash> -- <deleted-file>`  
➡️ Restores the deleted file from that commit.

---

## 🧠 Pro Tip:  
Use `git log --oneline` to view commit hashes you can use with `git checkout`.

---
# ↩️ Git Revert in Git

## 🔹 Revert a Specific Commit

**Undo a specific commit by creating a reverse commit:**  
`git revert <commit-hash>`  
➡️ Safely reverts the selected commit without changing history.

---

## 🔹 Revert the Latest Commit

**Undo the most recent commit (HEAD):**  
`git revert HEAD`  
➡️ Reverts only the latest commit and adds a new one that undoes it.

---

## 🔹 Revert a Range of Commits

**Revert multiple commits at once using a commit range:**  
`git revert <oldest-commit>^..<newest-commit>`  
➡️ Reverts everything from the oldest to the newest commit.

**Example:**  
git revert abc123^..def456


## 🔹 Revert a Range of Commits

**Revert multiple commits at once using a commit range:**  
`git revert <oldest-commit>^..<newest-commit>`  
➡️ Reverts from `abc123` to `def456`.

---

## 🔹 Revert a Merge Commit (With Optional No-Edit)

**Undo a merge commit safely by keeping a parent:**  
`git revert -m 1 <merge-commit-hash>`  
➡️ `-m 1` tells Git to keep the first parent branch's changes.  
⚠️ Must be used carefully to avoid conflicts.

**Skip commit message prompt when reverting (optional):**  
`git revert -m 1 --no-edit <merge-commit-hash>`  
➡️ Uses the default revert message without opening the editor.

---

## 🔹 Revert Multiple Commits One by One

**Revert selected commits individually in a single command:**  
git revert <commit1> <commit2> <commit3>

## 🧠 Pro Tip:

Unlike `git reset`, `git revert` is safe for **public branches**  
because it does **not rewrite history** — it just adds new commits that undo previous ones.

# 📦 Git Stash in Git

`git stash` temporarily saves uncommitted changes so you can work on something else  
and re-apply them later when needed.

---

## 🔹 Stash Your Changes

**Stash all modified tracked files:**  
`git stash`  
➡️ Saves current changes and resets your working directory.

**Stash with a custom message:**  
`git stash push -m "WIP: homepage design"`  
➡️ Helpful for remembering the stash purpose.

**Stash including untracked files:**  
`git stash -u`  
➡️ Also stashes files not yet added to Git.

**Stash including ignored files too:**  
`git stash -a`  
➡️ Saves tracked, untracked, and ignored files.

---

## 🔹 View Existing Stashes

**List all saved stashes:**  
`git stash list`  
➡️ Example output: `stash@{0}: On main: WIP homepage`

---

## 🔹 Apply a Stash (Keep It)

**Apply the latest stash without removing it:**  
`git stash apply`  
➡️ Useful if you want to reuse the stash later.

**Apply a specific stash by index:**  
`git stash apply stash@{1}`  
➡️ Applies that stash without deleting.

---

## 🔹 Apply and Remove (Pop)

**Apply and delete the latest stash:**  
`git stash pop`  
➡️ Shortcut for apply + delete.

---

## 🔹 Drop or Clear Stashes

**Delete a specific stash:**  
`git stash drop stash@{0}`

**Delete all stashes:**  
`git stash clear`  
➡️ Be careful! This removes all stash data permanently.

---

## 🧠 Pro Tip:

Use `git stash show -p stash@{0}` to see the exact changes  
stored in a stash before applying it. If you want to use another branch
stashed file is your branch you use easily 

---

# 🔀 Git Rebase in Git

`git rebase` ka use branch history ko linear aur clean banane ke liye hota hai.  
Ye ek branch ke commits ko doosri branch ke top par le jaata hai.

---

## 🔹 Rebase Current Branch onto Another

**Current branch ko kisi branch ke top par le jaane ke liye:**  
`git rebase <branch>`  
➡️ Jaise: `git rebase main`  
➡️ Current branch ke commits ko `main` ke latest commit ke baad attach karega.

---

## 🔹 Rebase While Checking Out

**Ek branch pe checkout karke rebase bhi karna:**  
`git checkout feature-branch`  
`git rebase main`  
➡️ `feature-branch` ke commits ko `main` ke latest point ke baad move karega.

---

## 🔹 Interactive Rebase (Edit History)

**Commit messages change karne, squash karne, delete karne ke liye:**  
`git rebase -i HEAD~3`  
➡️ Last 3 commits ke saath interactive rebase shuru karega.

**Common keywords in interactive mode:**  
- `pick` → Commit as it is use karo  
- `reword` → Commit message change karo  
- `edit` → Commit content edit karo  
- `squash` → Previous commit ke saath mila do  
- `drop` → Commit hata do

---

## 🔹 Abort, Skip, or Continue Rebase

**Rebase mein problem aaye toh:**  
- Rebase cancel karna ho:  
  `git rebase --abort`  
  ➡️ Sab kuch waise hi ho jaayega jaise rebase ke pehle tha.

- Conflict wale commit ko skip karna ho:  
  `git rebase --skip`

- Conflict resolve karne ke baad aage badhna ho:  
  `git rebase --continue`

---

## 🔹 Rebase vs Merge

| Feature       | Rebase                          | Merge                          |
|---------------|----------------------------------|--------------------------------|
| History       | Clean, linear                   | Complex, shows actual merges   |
| Use case      | Personal branches, clean logs   | Shared branches, team merges   |
| Risk          | History rewrite (careful!)      | No rewrite (safer)             |

---

## 🧠 Pro Tip:

✅ Rebase sirf **apni local ya personal branch** pe karo.  
❌ **Public/shared branches** ko rebase mat karo — ye unka pura history change kar deta hai.

---
# 🔖 Git Tags – One Page Cheat Sheet

Tags in Git are used to mark specific points in history — typically for releases.

---

## 🔹 Create a Lightweight Tag

**Just a name pointing to a commit (no extra metadata):**  
`git tag v1.0`  
➡️ Tags the latest commit as `v1.0`.

---

## 🔹 Create an Annotated Tag

**With tagger name, date, and message (recommended):**  
`git tag -a v1.0 -m "Release version 1.0"`  
➡️ Creates a full tag object stored in Git history.

---

## 🔹 Tag a Specific Commit

**Add a tag to an older commit:**  
`git tag -a v1.0 <commit-hash> -m "Release v1.0"`  
➡️ Tags that specific commit with `v1.0`.

---

## 🔹 View Tags

**List all tags in the repo:**  
`git tag`  
➡️ Shows all existing tags.

---

## 🔹 Show Tag Details

**Inspect tag metadata and the tagged commit:**  
`git show v1.0`  
➡️ Displays info and diff from the tag.

---

## 🔹 Delete Tags

**Delete a local tag:**  
`git tag -d v1.0`

**Delete a remote tag:**  
```bash
git push origin --delete v1.0
```

---

## 🔹 Push Tags to Remote

**Push a specific tag:**  
`git push origin v1.0`

**Push all local tags:**  
`git push --tags`

---

## 🔹 Checkout a Tag

**Switch to a tag (read-only detached HEAD state):**  
`git checkout v1.0`  
➡️ Useful for inspecting old releases.

---

## 🧠 Pro Tip:

Use **annotated tags** for releases — they are permanent objects  
and can include release notes and versioning history.

---
# 📜 Git Log – One Page Cheat Sheet

`git log` shows the commit history of the current branch or repository.

---

## 🔹 Basic Log

**Show default commit history (most recent first):**  
`git log`  
➡️ Displays commit hash, author, date, and message.

---

## 🔹 One-Line Format

**Show commits in single-line format:**  
`git log --oneline`  
➡️ Useful for a compact view.

---

## 🔹 Show Graph View

**See branch and merge history visually:**  
`git log --oneline --graph --all`  
➡️ Adds a visual representation of branches and merges.

---

## 🔹 Show Specific Author's Commits

**Filter commits by author:**  
`git log --author="Alice"`

---

## 🔹 Search in Commit Messages

**Find commits with specific keywords:**  
`git log --grep="fix"`

---

## 🔹 Show File History

**See commits that changed a specific file:**  
`git log <filename>`  
➡️ Shows the history of changes for that file.

---

## 🔹 Limit Number of Commits

**Show only N number of commits:**  
`git log -n 5`  
➡️ Displays the last 5 commits.

---

## 🔹 Show Patch/Diff with Commits

**Show changes introduced by each commit:**  
`git log -p`  
➡️ Useful to see actual code differences.

---

## 🔹 Format Log Output

**Customize log output format:**  
`git log --pretty=format:"%h - %an, %ar : %s"`  
➡️ Custom log format: hash, author, time, message.

---

## 🧠 Pro Tip:

Use `git log --stat` to see summary of changes (files modified, lines added/removed).

Combine flags for powerful history insights:
```bash
git log --oneline --graph --decorate --all
```

---

# Git Log

## Useful Options

These options can be added to `git log` to enhance the output and help with understanding commit history better.

- `--graph` : Visualize branches and merges in a text-based graph format.
- `--oneline` : Show each commit on a single line (useful for compact views).
- `--all` : Show all references, including other branches and remotes.
- `--decorate` : Show ref names (like branches or tags) next to commits.
- `--name-only` : Show only the names of changed files.
- `--name-status` : Show names and the status of changed files.
- `--pretty` : Format the log output (e.g., `--pretty=oneline`, `--pretty=format:"..."`).
- `--numstat` : Show number of insertions and deletions per file.
- `--stat` : Show statistics for each commit (number of changes, files, etc.).
- `--status` : Show the status of changed files.

> 💡 Use combinations like:  
> `git log --oneline --graph --all --decorate`  
> for a great overview of commit history with branches and merges.

# Git Log with `--pretty=format`

The `--pretty=format` option allows you to customize how the `git log` output appears. You can use various placeholders to format commit data.

## Useful Placeholders

| Format Code     | Description                                             |
|-----------------|---------------------------------------------------------|
| `%H`            | Full commit hash                                        |
| `%h`            | Abbreviated (7-digit) commit hash                       |
| `%ad`           | Author date                                             |
| `%cd`           | Committer date                                          |
| `%an`           | Author name                                             |
| `%ae`           | Author email                                            |
| `%s`            | Subject (first line of commit message)                  |
| `%b`            | Body (remaining part of commit message)                 |
| `%n`            | New line                                                |
| `%<(<N>)`       | Left-align within N columns                             |
| `%>(<N>)`       | Right-align within N columns                            |
| `%Cred`         | Start red color formatting                              |
| `%Cgreen`       | Start green color formatting                            |
| `%C(...)`       | Custom color (e.g., `%C(bold red)`)                     |
| `%Creset`       | Reset color to default                                  |

## Example

```bash
git log --pretty=format:"%h %<(<20>)%an %s"

```

# Some Important Topic

## 🔹 Explanation: `git show HEAD~2:file1.txt > newfile.txt`

### ✅ Command:

```bash
git show HEAD~2:file1.txt > newfile.txt
```

---

## 🔹 What It Does

This command retrieves the content of `file1.txt` as it existed **two commits ago** and saves it to a new file called `newfile.txt` in your current working directory.

---

## 🔹 Breakdown

**HEAD~2:file1.txt**  
➡️ Refers to `file1.txt` exactly two commits before the latest commit.  
Git will extract the state of that file from that specific commit.

**git show**  
➡️ Displays the content from Git’s history.

**> (redirect operator)**  
➡️ Sends the output (the old file content) into a new file instead of showing it on the terminal.

**newfile.txt**  
➡️ This is the output file where the previous version will be stored.

---

## 🔹 Result (Output)

If `file1.txt` had the content:

```
Hello from two commits ago
```

Then after running the command:

- A new file named `newfile.txt` will be created.
- It will contain the same content from `file1.txt` **two commits ago**.

---

## 🔹 Why It's Useful

📁 Restore an older version of a file without affecting the current version.  
🔍 Compare past and present versions side-by-side.  
✅ Reuse specific code or content from Git history.

---

## 📝 Tip

You can adjust the number in `HEAD~2` to go further back:

- `HEAD~1` → one commit before current  
- `HEAD~3` → three commits before current  
- and so on...

---

# 🔹 Explanation: `git cherry-pick`

### ✅ What It Does

The `git cherry-pick` command **applies the changes introduced by a specific commit** from another branch into your current branch — **without merging the entire branch**.

---

## 🔹 Basic Syntax

```bash
git cherry-pick <commit-hash>
```

➡️ This takes a specific commit and **applies it on top of the current branch**.

---

## 🔹 Example Use Case

Let’s say your branch history looks like this:

```
main:          A---B---C
                 \
feature-xyz:      D---E
```

You are currently on `main` and want to apply only commit `E` from `feature-xyz` without merging the whole branch.

```bash
git cherry-pick <E-commit-hash>
```

➡️ This will bring only the changes from commit `E` into your `main` branch.

---

## 🔹 Apply Multiple Commits

You can also cherry-pick multiple commits:

```bash
git cherry-pick <hash1> <hash2>
```

Or a range of commits:

```bash
git cherry-pick A..E
```

➡️ This applies all commits **after A up to and including E**.

---

## 🔹 Cherry-Pick with Conflict

If the commit you're cherry-picking conflicts with your current code:

1. Git will pause and show the conflict.
2. You must manually fix the conflict.
3. Then run:
   ```bash
   git add .
   git cherry-pick --continue
   ```

---

## 🔹 Abort Cherry-Pick (if something goes wrong)

```bash
git cherry-pick --abort
```

➡️ This will cancel the cherry-pick and revert your branch back to its previous state.

---

## 🔹 Why It's Useful

✅ Apply specific fixes or features across branches  
🔍 Avoid merging unwanted history  
⚙️ Isolate useful commits from messy branches

---

# 🔹 Explanation: `git reflog`

### ✅ What It Does

The `git reflog` command shows a **log of where your HEAD and branch references have been**, including moves, checkouts, commits, resets, merges, rebases — everything, even if it's not in `git log`.

---

## 🔹 Basic Syntax

```bash
git reflog
```

➡️ Shows a list of all actions that have moved your `HEAD` — each with a reference ID and message.

---

## 🔹 What the Output Looks Like

Example:

```
c3e2b1d HEAD@{0}: commit: Added new feature
a8f6d1c HEAD@{1}: checkout: moving from feature to main
b9a8ddf HEAD@{2}: commit: Initial commit
```

- `HEAD@{0}` → Most recent action  
- `HEAD@{1}` → One step before  
- And so on…

Each reflog entry includes:
- Commit hash
- Reflog index (`HEAD@{n}`)
- Action (e.g., commit, checkout)
- Message

---

## 🔹 Restore Lost Commits (Undo Mistakes)

### ✅ Example Use Case:

Let’s say you did a `git reset --hard` and lost work.

You can run:

```bash
git reflog
```

Find the commit you want to recover, then:

```bash
git checkout <commit-hash>
```

Or to restore your branch:

```bash
git reset --hard <commit-hash>
```

✅ This is one of the most powerful recovery tools in Git!

---

## 🔹 Cleanup Reflog (Optional)

To clean old entries (⚠️ use carefully):

```bash
git reflog expire --expire=30.days.ago --all
git gc --prune=now
```

---

## 🔹 Why It's Useful

🔁 View the full history of HEAD movement (not just commits)  
🛠️ Recover lost commits after reset or rebase  
🔍 Track all Git actions, even ones not stored in `git log`

---
