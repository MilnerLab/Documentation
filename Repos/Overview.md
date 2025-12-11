# Lab Project Overview

All lab projects in this repository follow the same basic structure and setup workflow.  
This document explains **what each important file is for** and **how to get a project ready to run**.

---

## 1. Common Project Structure

Typical contents of a lab project:

- `README.md` – project-specific information (what the app does, how to use it)
- `setup_env.ps1` – [PowerShell script](#4-environment-setup-script-setup_envps1) to set up the development environment
- `.venv/` – Python [virtual environment](..\General\Python\Working%20with%20Python.md##-2.-virtual-environments) (created by `setup_env.ps1`)
- `.vscode/` – [VS Code settings](..\General\Visual%20Studio%20Code\Working%20with%20VS%20Code.md##-what-the-vscode-folder-is) (debug configs, tasks, etc.)
- `_requirements.txt` – list of Python packages for this project
- `_extensions.txt` – list of VS Code extensions recommended for this project
- `*.code-workspace` – optional [VS Code workspace](#3-vs-code-workspace-code-workspace) file for this project

---

## 2. README.md

Each project has its own `README.md`.

It usually contains:

- A short description of what the project is about
- Notes about how to run or test the app
- Links to more detailed documentation (if available)

> **Tip:** Always read the project’s `README.md` first. It may contain project-specific details that are not covered here.

---

## 3. VS Code Workspace (`*.code-workspace`)

Some projects include a `*.code-workspace` file, for example:

- `Lab_Apps.code-workspace`

This file contains:

- Which folder(s) to open in VS Code
- Workspace-specific settings
- Recommended extensions for this workspace

### How to use it

Instead of opening the folder directly, **open the workspace file**:

- From VS Code:  
  `File → Open Workspace from File...` → select `*.code-workspace`
- Or double-click the `*.code-workspace` file from your file explorer

> **Recommendation:** If a workspace file exists, always use it.  
> It ensures VS Code has the correct settings for this project.

---

## 4. Environment Setup Script (`setup_env.ps1`)

Every project has a `setup_env.ps1` script in the project root.

This script is responsible for:

1. **Creating a Python virtual environment** (`.venv/`) if it does not exist.
2. **Installing Python dependencies** from `_requirements.txt`.
3. **Installing VS Code extensions** listed in `_extensions.txt` (only if they are not already installed).

### How to run the script

1. Open **PowerShell**.
2. Navigate to the project folder (if not already in it):

    ```powershell
   cd path\to\your\project
    ```

3. Run the setup script:

   ```powershell
   . .\setup_env.ps1
   ```

### When to run `setup_env.ps1`

* **First time** you work with the project on a new machine
* After pulling changes where `_requirements.txt` or `_extensions.txt` was updated

The script is designed so you can safely run it again; it will only create / install what is missing.
