
# Installing Python

This guide explains how to install **Python 3** globally on Windows.

---

## 1. Download Python Installer

1. Open: https://www.python.org/downloads/latest/pymanager/
2. Click **“Download Installer (MSIX)”**.

and install it.

---


## 2. Install Python versions

To install a python version (for example `3.13.x`) you need to run:

```powershell
py install 3.13
```
This will install the latest `3.13.x` version.

If you need to install a specific python version (for example the `x32` bit) you can run:

```powershell
py install 3.13-32
```

List what you have installed (and what’s “current”):

```powershell
py list
```

### If `py` isn’t working

* Run the built-in config checker:

  ```powershell
  py install --configure
  ```
* If you have the **legacy “Python launcher”** installed, it may “steal” the `py` command—uninstall it from *Installed apps* (or use `pymanager ...` to avoid conflicts). ([Python documentation][2])

[1]: https://www.python.org/downloads/latest/pymanager/ "Python Release Python install manager 25.2 | Python.org"
[2]: https://docs.python.org/3/using/windows.html "4. Using Python on Windows — Python 3.14.2 documentation"
