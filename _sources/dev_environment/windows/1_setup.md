# Install Setup Software

(devenv:windows:powershell)=
## Install PowerShell
You will install PowerShell first. We'll work with PowerShell later in the semester, but we'll use it now to help install other software.

1. [PowerShell installation instructions](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.3)
    * If your computer does not have "Winget", use the MSI package installer

```{important}
Restart your computer after installing PowerShell!
```
---
(devenv:windows:chocolatey)=
## Install Chocolatey (a Windows package manager)
1. Run PowerShell *as an administrator* on your computer
2. Copy and paste the following command into PowerShell:

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```