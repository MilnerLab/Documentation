
# Working with VS Code & the `.vscode` Folder

When you work on a project with **Visual Studio Code**, most project-specific configuration lives in the `.vscode` folder at the root of your repo.

## What the `.vscode` Folder Is

The `.vscode` folder contains JSON files that tell VS Code how to behave **for this project only**.  
These settings are usually committed to Git so the whole team shares the same configuration.

Typical files:

### `settings.json`
Project-specific editor settings, e.g.:

- Indentation (`tabSize`, `insertSpaces`)
- Default formatter (Prettier, Black, etc.)
- Language-specific settings (for Python, JS, etc.)

```json
{
  "editor.tabSize": 2,
  "editor.formatOnSave": true
}
```

---

### `launch.json`

Debug configurations:

* Which file or program to start
* Environment variables
* Arguments
* Browser / runtime (Node, Python, etc.)

```json
{
  "configurations": [
    {
      "name": "Launch App",
      "type": "node",
      "request": "launch",
      "program": "${workspaceFolder}/index.js"
    }
  ]
}
```

---

### `tasks.json`

Defines custom tasks you can run from VS Code:

* Build commands
* Test commands
* Linting or formatting scripts

```json
{
  "tasks": [
    {
      "label": "Run tests",
      "type": "shell",
      "command": "npm test"
    }
  ]
}
```

---

### `extensions.json`

Recommended extensions for this workspace.
VS Code will suggest installing them when someone opens the project.

```json
{
  "recommendations": [
    "dbaeumer.vscode-eslint",
    "esbenp.prettier-vscode"
  ]
}
```
