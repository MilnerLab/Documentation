# Working with Python

## 1. Run vs Debug

When you execute Python code, there are two main modes: **Run** and **Debug**.  
They both execute your program, but with different goals.

### 1.1 Run (Normal Execution)

**What it is:**

- Runs your script from start to finish as fast as possible.
- No special tools for inspecting what happens inside, beyond normal prints and error messages.

**How it looks:**

Terminal example:

```bash
python main.py
```

In VS Code:

* Click the **Run** button, or
* Use the integrated terminal and run `python main.py`.

**Characteristics:**

* Good for when your code already works and you just want to execute it.
* If an error occurs, the program stops and shows a traceback.

---

### 1.2 Debug (Run with a Debugger)

**What it is:**

Debugging means running your program under a **debugger**, which gives you control and insight into what the code does while it runs.

**What you can do in Debug mode:**

* Set **breakpoints** – lines where the program will pause.
* **Step through** code line by line (step over, step into, step out).
* Inspect **variables** and their values at each pause.
* See the **call stack** (which functions called which).
* Evaluate small expressions while paused.

**In VS Code:**

* Open the **Run and Debug** view (or press `F5`).
* Choose / configure a debug configuration (via `.vscode/launch.json`).
* Start debugging and watch the program stop at breakpoints.

**When to use it:**

* When something doesn’t work and you don’t know why.
* When you want to understand how a piece of code behaves step by step.

---

## 2. Virtual Environments

### 2.1 What Is a Virtual Environment (`venv`)?

A **virtual environment** (often called *venv*) is an isolated Python environment **inside your project folder**.

It has its own:

* Python interpreter
* Installed packages (`pip install ...`)
* Dependency versions

This isolation means:

* Each project can have its **own dependencies** and versions.
* It does not interfere with your **global** Python installation.
* Different projects don’t break each other.


**Make projects reproducible:**
  You can save dependencies to `_requirements.txt` and recreate the same environment on another machine.


---

### 2.2 Creating a Virtual Environment

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

**Windows (PowerShell):**

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

### 2.6 Using `venv` together with Run & Debug

* **Always activate the venv** before running or debugging your project in a terminal.
* In VS Code, make sure the **Python interpreter** is set to the one from `.venv` (shown in the status bar at the bottom).
* Then, both **Run** and **Debug** will use the correct dependencies from your virtual environment.
