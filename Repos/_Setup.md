# Setup the Enviroment

Every repository has its own `setup_env.ps1` script. You only have to run it, if you want to compile files from that repository (for example you may not want to run Base_Lib on its own, so you don't have to run the setup). 

## Environment Setup Script (`setup_env.ps1`)

Every project has a `setup_env.ps1` script in the project root.

This script is responsible for:

1. **Creating a Python virtual environment** (`.venv/`) if it does not exist.
2. **[Installing Python dependencies](..\General\Python\Working%20with%20Python.md#2.-virtual-environments)** from `_requirements.txt`.
3. **[Installing VS Code extensions](..\General\Visual%20Studio%20Code\Working%20with%20VS%20Code.md#extension.json)** listed in `_extensions.txt` (only if they are not already installed).

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