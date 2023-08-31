# Establish a Root Directory and Install Git on Windows

(devenv:windows:rootdirectory)=
## Create a Root Directory 
You will create a directory that you will use as your **root directory** for this course. This directory can be anywhere on your computer. We will refer to your **root directory** through the remainder of the semester.

```{important}
File management is going to be **extremely** important in this course! Please be aware of the specific file and directory paths that are used
```

1. Create a directory with the name `cit30900` somewhere on your computer that makes sense to you (e.g. `Documents` or `OneDrive`).

(devenv:windows:git)=
## Install Git on Windows

You can install Git on Windows in one of two ways.

(devenv:windows:install_git_chocolatey)=
### Option 1: Use Chocolatey to Install Git
1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to install Git:

```
choco install git
```
3. Answer `Y` to each script installation (or `A` to accept all at once)

(devenv:windows:install_git_windows)=
### Option 2: Use the Downloadable Installer to Install Git

1. [Download the latest version of Git for Windows here](https://gitforwindows.org/) and follow all of the instructions in the installer.

2. You may accept the default value for all of the options.

3. **Ensure you select the Git Bash option (if asked) during the installation** (This will be important later.)