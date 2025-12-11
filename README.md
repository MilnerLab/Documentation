# Milner Lab Documentation

This repository serves as the **central documentation hub for all code and projects developed at Milner Lab**.

It should be used to document everything from setting up Visual Studio Code to running the applications.

---

## Projects

This repository is intended to cover documentation for all the python projects in the Milner Lab:

- [Lab_Apps](./Repos/Lab_Apps/General%20Information.md)
- LabView_To_Python
- [Phase_Stabilization](./Repos/Phase_Stabilization/General%20Information.md)
- [Base_Lib](./Repos/Base_Lib/General%20Information.md)

If you want to know more about the project setup click [here](./Repos/Overview.md).

---

## Getting Things Set Up

This section should give the guideline on how to set up your computer to work and run any of the [projects](#projects) from the Milner Lab.

### 1. Installing VS Code
- follow the [instructions](./General/Visual%20Studio%20Code/Setup.md#vs-code-setup--cloning-a-github-repository) and install VS Code

### 2. Installing Git 
- follow the [instructions](./General/Git%20and%20GitHub/Setup.md###-1.-install-git) and install/ setup Git

### 3. Installing Python
- follow the [instructions](./General/Python/Setup.md#installing-python) and install python (version 3.13.x)
- read the python requirements for the project ([Phase_Stabilization](./Repos/Phase_Stabilization/General%20Information.md##python), [Lab_Apps](./Repos/Lab_Apps/General%20Information.md##python))

### 4. Cloning the Repositories
- clone the repositories either by using [git commands](./General/Git%20and%20GitHub/Setup.md#3-clone-a-repository-to-your-computer) or recommended directly in [VS Code](./General/Visual%20Studio%20Code/Working%20with%20VS%20Code.md#clone-a-github-repository-directly-in-vs-code)
- read the dependency requirements for the project ([Phase_Stabilization](./Repos/Phase_Stabilization/General%20Information.md#dependencies), [Lab_Apps](./Repos/Lab_Apps/General%20Information.md#dependencies))

### 5. Setting up the Environment
- run the `setup_env.ps1` as described in the [instruction](./Repos/Overview.md#4-environment-setup-script-setup_envps1)