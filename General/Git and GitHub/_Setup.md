# Setup Git

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


