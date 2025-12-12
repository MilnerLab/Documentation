# Lab Project Overview

All lab projects follow the same basic structure and setup workflow.  
This document explains **what each important file is for**.

---

## 1. Common Project Structure

Typical contents of a lab project:

- `README.md` – project-specific information (what the app does, how to use it)
- `setup_env.ps1` – [PowerShell script](#4-environment-setup-script-setup_envps1) to set up the development environment
- `.venv/` – Python [virtual environment](..\General\Python\Working%20with%20Python.md#-2.-virtual-environments) (created by `setup_env.ps1`)
- `.vscode/` – [VS Code settings](..\General\Visual%20Studio%20Code\Working%20with%20VS%20Code.md#-what-the-vscode-folder-is) (debug configs, tasks, etc.)
- `_requirements.txt` – list of Python packages for this project
- `_extensions.txt` – list of VS Code extensions recommended for this project
- `*.code-workspace` – optional [VS Code workspace](#3-vs-code-workspace-code-workspace) file for this project



