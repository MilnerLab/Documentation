# Virtual Environments

## What Is a Virtual Environment (`venv`)?

A **virtual environment** (often called *venv*) is an isolated Python environment **inside your project folder**.

It has its own:

* Python interpreter
* Installed packages (`pip install ...`)
* Dependency versions

This isolation means:

* Each project can have its **own dependencies** and versions.
* It does not interfere with your **global** Python installation.
* Different projects don’t break each other.

---

### 1. Creating a Virtual Environment

From your project folder:

**Windows (PowerShell):**

```powershell
py -3 -m venv .venv
```

**macOS / Linux:**

```bash
python3 -m venv .venv
```

This creates a `.venv` directory containing the isolated Python environment.

---

### 2. Activating the Virtual Environment
You have to be in the folder where the `.venv` folder is located.

**Windows (Terminal):**

```powershell
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux:**

```bash
source .venv/bin/activate
```

If activation worked, your shell prompt usually starts with something like:

```text
(.venv) ...
```

Now, when you run:

```bash
python --version
pip install <package>
```

these commands use the Python and `pip` **inside** the virtual environment, not the global ones.

---

#### Saving the Environment

**Make projects reproducible:**
  You can save dependencies to `_requirements.txt` and recreate the same environment on another machine.
  ```powershell
  python -m pip freeze > _requirements.txt
  ```
This will take a snapshot of the current environment (all the libraries and their versions)