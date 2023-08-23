# Establish a Virtual Environment

You will create a virtual environment to use in this course. This environment will manage all the Python packages that are installed throughout the course so that you can easily uninstall them all later if needed.

(devenv:mac:install_virtualenv)=
## Install virtualenv

1. Open a Terminal window on your computer
2. Use the following command to install virtualenv:

```
brew install virtualenv
```

(devenv:mac:virtualenvwrapper)=
## Install virtualenvwrapper
You'll also install a helper package that simplifies many of the commands related to your virtual environment.

1. Open a Terminal window on your computer
2. Use the following command to install virtualenvwrapper:

```
brew install virtualenvwrapper
```

We'll now add the virtualenvwrapper command to your shell configuration.

3. At the Terminal command line, enter the following:

```
nano ~/.zshrc
```

This will open a text-based file editor with your *shell* configuration.

4. Use the keyboard (not your mouse) to navigate to the end of the file and add the following line:

```
source virtualenvwrapper.sh
```

3. Save and exit the file by pressing `Control+X` (**not** `Command`), and then type `Y` and `Enter` to confirm the changes.

4. Restart your shell by entering the following command on the command line:

```
source ~/.zshrc
```

(devenv:mac:create_virtualenv)=
## Create Your Virtual Environment

Use `virtualenvwrapper` to create a new virtual environment for this course.

1. In the Terminal, use the following command to create a virtual environment named `cit30900env`:

```
mkvirtualenv cit30900env
```

The previous command created **and activated** your virtual environment. You will know that your environment is activated because its name appears in parentheses before your command prompt in the terminal window. See the example below:

```{image} ../img/mac-active-ve.png
:alt: An active virtual environment displayed at the command prompt
:align: center
```

(devenv:mac:use_virtual_environment)=
## Use Your Virtual Environment
If your virtual environment is not currently running, you can easily start it.

1. Open a Terminal window on your computer
2. Use the following command to start your virtual environment named `cit30900env`:

```
workon cit30900env
```

```{image} ../img/mac-active-ve.png
:alt: An active virtual environment displayed at the command prompt
:align: center
```