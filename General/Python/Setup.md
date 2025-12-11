
# Installing Python

This guide explains how to install **Python 3** globally on Windows so that you can run it from PowerShell using the `py` launcher (e.g. `py -3 script.py`).

---

## 1. Download Python

1. Open: https://www.python.org/downloads/windows/
2. Click **“Download Python 3.x.x”** (the latest stable 3.x version).

Save the installer (`python-3.x.x-amd64.exe`) and run it.

---

## 2. Important Installer Options (Windows)

When the installer window opens:

1. At the bottom of the first screen, **check**:

   - ✅ **Add python.exe to PATH**  
   - ✅ **Use admin privileges when installing py.exe** (if shown)

2. Click **“Customize installation”** (recommended).

3. On the next screen, make sure these are checked:

   - ✅ **pip**
   - ✅ **py launcher** (this installs the `py` command)

4. Click **Next** and then:

   - Choose **“Install for all users”** if possible
   - Keep the default install location (e.g. `C:\Program Files\Python311\`)
   - Click **Install**

When it finishes, close the installer.

---

## 3. Verify in PowerShell

Open a new **PowerShell** window and run:

```powershell
py --version
py -3 --version
```

You should see something like:

```text
Python Launcher for Windows
Python 3.x.x
```

If that works, you can run Python 3 via:

```powershell
py -3
py -3 your_script.py
```

> Note: The `py` launcher lets you specify the Python version (`-3`, `-3.11`, etc.), which is very handy if your script explicitly calls `py -3 ...`.

