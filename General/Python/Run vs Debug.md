# Run vs Debug

When you execute Python code, there are two main modes: **Run** and **Debug**.  
They both execute your program, but with different goals.

## 1. Run (Normal Execution)

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

## 2. Debug (Run with a Debugger)

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