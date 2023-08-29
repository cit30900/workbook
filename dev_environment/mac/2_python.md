# Install Python on MacOS

Python is the primary programming language we will use in this course (although there will be others). You will install Python and learn how to use it within a virtual environment to complete your assignments for this course.

(devenv:mac:install_python)=
## Use Homebrew to Install Python
1. Open a Terminal on your computer
2. Use the following command to install Git:

```
brew install python
```

3. Confirm that Python is installed by typing the following commands:

```
pip3 --version
```

This should return a message similar to `pip 23.2.1 from /usr/local/lib/python3.11/site-packages/pip (python 3.11)`

```
python3 --version
```

This should return a message similar to `Python 3.11.4`. (Your version number may be higher, which is fine.)

(devenv:mac:alias_python)=
## Create Aliases for pip and Python

The two instructions above appended a "3" to the end of the program names. `pip3` is a program that installs Python packages on your computer. `python3` will run Python programs.

You can easily create aliases that allow you to use `pip` and `python` instead of the `pip3` and `python3` commands.

1. At the Terminal command line, enter the following:

```
nano ~/.zshrc
```

This will open a text-based file editor with your *shell* configuration.

2. Use the keyboard (not your mouse) to navigate to the end of the file and add the following lines:

```
alias python=python3
alias pip=pip3
```

3. Save and exit the file by pressing `Control+X` (**not** `Command`), and then type `Y` and `Enter` to confirm the changes.

4. Restart your shell by entering the following command on the command line:

```
source ~/.zshrc
```

5. Test your new aliases with the following commands:

```
pip --version
```

```
python --version
```

These should both return the same results as they did previously.