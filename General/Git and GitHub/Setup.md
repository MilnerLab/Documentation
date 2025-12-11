# Getting Started with Git

This short guide explains how to install Git.

---

## 1. Install Git

### Windows
1. Go to the official Git website: <https://git-scm.com/>
2. Download the installer for Windows.
3. Run it and accept the default options.

### macOS
You have two common options:

- **Using Homebrew** (if you have it):
    ```bash
    brew install git
    ```
- Else do the same thing as for Windows
## 2. Configure Git (one-time setup)

Open a terminal (or Git Bash on Windows) and set your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

You can check your settings with:

```bash
git config --list
```

---
# Getting Started with GitHub

This short guide explains how to create and clone repositories from GitHub.

---

## 1. Create a GitHub Account

1. Go to <https://github.com/>
2. Click **Sign up**.
3. Choose a username, enter your email, and set a password.
4. Confirm your email address.


## 2. Create a New Repository on GitHub

1. After logging in, click the **+** button in the top-right corner.
2. Select **New repository**.
3. Enter a **Repository name**.
4. Choose whether it should be **Public** or **Private**.
5. (Optional) Add a description.
6. Click **Create repository**.

You will now see a page with the URL of your new repository, for example:

```text
https://github.com/USERNAME/REPO-NAME.git
```


## 3. Clone a Repository to Your Computer

To get a copy of a repository on your machine:

1. On the repository page on GitHub, click the **Code** button.

2. Copy the **HTTPS** URL (for example: `https://github.com/USERNAME/REPO-NAME.git`).

3. Open a terminal, go to the destination folder and run:

    ```bash
    git clone https://github.com/USERNAME/REPO-NAME.git
    ```

You now have a **local** copy of the repository on your computer.

