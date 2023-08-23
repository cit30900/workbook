# Establish a Virtual Environment

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

```{image} ../img/win-active-ve.png
:alt: An active virtual environment displayed at the command prompt
:align: center
```

(devenv:windows:use_virtual_environment)=
## Use Your Virtual Environment
If your virtual environment is not currently running, you can easily start it.

1. Open a Command Prompt *as an adminstrator* on your computer
2. Use the following command to start your virtual environment named `cit30900env`:

```
workon cit30900env
```

```{image} ../img/win-active-ve.png
:alt: An active virtual environment displayed at the command prompt
:align: center
```