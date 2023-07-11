# Creating a Development Environment on Windows

Follow the steps below to install the software you will need for this course.

You must be running Windows 10 or 11 for this software to run.

```{important}
You will need to know the administrator username and password for your computer for some of these installations!
```

Steps to set up your development environment:
1. {ref}`devenv:windows:powershell`
2. {ref}`devenv:windows:chocolatey`
3. {ref}`devenv:windows:python`

(devenv:windows:powershell)=
## Install PowerShell
You will install PowerShell first. We'll work with PowerShell later in the semester, but we'll use it now to help install other software.

1. [PowerShell installation instructions](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.3)
    * If your computer does not have "Winget", use the MSI package installer

```{important}
Restart your computer after installing PowerShell!
```

(devenv:windows:chocolatey)=
## Install Chocolatey (a Windows package manager)
1. Run PowerShell *as an administrator* on your computer
2. Copy and paste the following command into PowerShell:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

(devenv:windows:python)=
## Use Chocolatey to Install Python
1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to install Python:

```
choco install python
```
3. Answer `Y` to each script installation (or `A` to accept all at once)

```{important}
Restart your computer after installing Python!
```

(devenv:windows:virtualenv)=
## Install virtualenv
You will create a virtual environment to use in this course. This environment will manage all the Python packages that are installed throughout the course so that you can easily uninstall them all later if needed.

1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to install virtualenv:

```
pip install virtualenv
```

(devenv:windows:virtualenvwrapper-win)=
## Install virtualenvwrapper-win
You'll also install a helper package that simplifies many of the commands related to your virtual environment.

1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to install virtualenvwrapper-win:

```
pip install virtualenvwrapper-win
```

(devenv:windows:virtualenvironment)=
## Create a Virtual Environment
Use `virtualenvwrapper-win` to create a new virtual environment for this course.

1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to create a virtual environment named `cit30900env`:

```
mkvirtualenv cit30900env
```

The previous command created **and activated** your virtual environment. You will know that your environment is activated because its name appears in parentheses before your command prompt in the terminal window. See the example below:

```{image} img/win-active-ve.png
:alt: An active virtual environment displayed at the command prompt
:align: center
```

(devenv:windows:rootdirectory)=
## Create a Root Directory 
You will create a directory that you will use as your **root directory** for this course. This directory can be anywhere on your computer. We will refer to your **root directory** through the remainder of the semester.

```{important}
File management is going to be **extremely** important in this course! Please be aware of the specific file and directory paths that are used
```
