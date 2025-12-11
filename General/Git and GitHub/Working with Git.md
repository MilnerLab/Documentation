# Git – Short Overview and Key Terms

Git is a **version control system**.  
It helps you track changes to files (usually source code), move backwards in history, and collaborate with others without overwriting each other’s work.

The Command line examples given in this document are the basic git commands. However, there are a few UIs that make it way easier to handle git. In our case we can use the VS-Code integration.

You typically have:

- A **local repository** on your own machine
- A **remote repository** on a server (e.g. GitHub, GitLab, Bitbucket)

You edit files, mark them to be saved, create snapshots of the project, and then synchronize those snapshots with the remote repository.

---

## Basic Workflow

1. **Edit files** in your working directory.
2. **Stage** the changes (tell Git which changes you want to include).
3. **Commit** the staged changes (create a snapshot in your local repo).
4. **Push** your commits to the remote repo so others can see them.
5. **Pull** changes from the remote repo to update your local repo.

---

### 1. Commit

A **commit** is a snapshot of your project at a certain point in time.

- Contains:
  - The changes you made
  - A **commit message**
  - Metadata (author, date, etc.)
- Commits are stored in your **local** repository.

Command example:

```bash
git commit -m "Add login feature"
```

---

### 2. Commit Message

A **commit message** describes what changed in that commit.

* Should be **short and clear**
* Helps you and others understand the project history later

Example of a good message:

> "Fix bug in user registration validation"

---

### 3. Stage / Staging (Index)

To **stage** changes means to select which changes you want to include in the next commit.

* The staging area is also called the **index**.
* You can stage some files and not others.

Command example:

```bash
git add file1.js file2.css
```

Now `file1.js` and `file2.css` are staged for the next commit.

---

### 4. Push

**Push** sends your local commits to the remote repository.

* Makes your changes visible to others.
* Only commits (not unstaged or uncommitted changes) are pushed.

Command example:

```bash
git push origin main
```

This pushes the commits from your local `main` branch to the remote `main` branch on `origin` (usually GitHub/GitLab).

---

### 5. Pull

**Pull** fetches changes from the remote repository and merges them into your current branch.

* It is basically:

  * `git fetch` (download new commits)
  * plus `git merge` (combine them with your local branch)

Command example:

```bash
git pull origin main
```

This updates your local `main` with new commits from the remote `main`.

---

### 6. Merge

**Merge** combines the history of one branch into another.

* Example: you have a `feature` branch and want to bring its changes into `main`.
* Git tries to automatically combine all changes.

Command example:

```bash
git checkout main
git merge feature
```

Now `main` contains the changes from `feature` (if no conflicts).


#### Merge Conflict

A **merge conflict** happens when Git cannot automatically merge changes.

Typical case:

* You and someone else both changed **the same lines** in the same file on different branches.
* Git doesn’t know which version is correct.

What you do:

1. Git marks the conflict in the file with `<<<<<<<`, `=======`, `>>>>>>>`.
2. You manually edit the file to choose or combine the changes.
3. Then you stage the fixed file and commit.

Example flow:

```bash
# after a merge produces conflicts
# edit the files to resolve the conflict
git add conflicted_file.js
git commit -m "Resolve merge conflict in conflicted_file.js"
```

---
---

# `.gitignore` Basics

A `.gitignore` file tells Git which files and folders it should **ignore** (not track).

## Why use `.gitignore`?

- Avoid committing temporary or generated files  
- Keep secrets (API keys, credentials) out of your repo  
- Reduce noise in `git status`

## Where to put it?

- Create a file named `.gitignore` in the **root** of your repository.
- Git will apply the rules to that repo.

## Common Examples

```gitignore
# Node.js
node_modules/
dist/

# Python
__pycache__/
*.pyc
.env

# Logs & OS files
*.log
.DS_Store

# IDE / Editor
.vscode/
.idea/
```

## Patterns

* `file.txt` — ignore a specific file
* `folder/` — ignore a folder
* `*.log` — ignore all `.log` files
* `!keep.log` — **do not ignore** `keep.log` even if `*.log` is ignored

## Important

* `.gitignore` only affects **untracked** files.
* If a file is already tracked, remove it first:

```bash
git rm --cached path/to/file
```

Then Git will start ignoring it according to `.gitignore`.
