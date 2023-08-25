# Use the Command Prompt in Visual Studio Code

Now that you have VS Code installed, you can use its user interface to create and edit files as well as interact with the Command Line.

(devenv:windows:vscode_terminal_default)=
## Set the Default Terminal in Visual Studio Code

The terminal in VS Code can be set to the Windows Command Prompt or PowerShell. For now, it's best if you set it to the Command Prompt.

1. In VS Code, press `Control + Shift + P` to open the Command Palette.

2. Start to type the following and select it when it appears: `Terminal: Select Default Profile`

3. Select `Command Prompt`

4. Quit and restart VS Code

(devenv:windows:vscode_panel)=
## Open a Terminal in Visual Studio Code

You can split the VS Code view to show both the file editor as well as the command line. To do this, you will open the bottom panel in VS Code and show the Terminal.

1. From the top right of the menu bar in VS Code, choose the `Toggle Panel` icon:

    ```{image} ../img/vscode_toggle_panel.png
    :alt: Visual Studio Code's toggle panel icon
    :align: center
    :width: 200px
    ```

  * Alternatively, you can press `Ctrl+J`

2. If it is not already selected, choose the "Terminal" tab at the top of the VS Code panel.

    ```{image} ../img/vscode_terminal.png
    :alt: Visual Studio Code's tab bar in the panel with the Terminal (4th tab) highlighted
    :align: center
    :width: 400px
    ```

3. You should now see Windows command prompt in the Terminal within VS Code. Your terminal prompt will be unique to you, but may be as simple as `C:\Users\Username>`. This is where you can issue instructions to the command prompt.

(devenv:windows:root_directory)=
## Create a Root Directory for this Course

Create a root directory on your computer that you will use as your "home base" for all of the files you work with in this course.

```{note}
You will hear me refer to this specific directory as your "root directory" or "local root directory" throughout this course!
```

By default, your Terminal prompt is at the user's home directory in Windows. You can create a new directory at this location or you can create a directory somewhere else on your computer.

You can create your root directory in one of two ways: through the command line, or through the Graphical User Interface.

(devenv:windows:root_directory:terminal)=
### Option 1: Create a Root Directory Using the Command Line

1. From the Terminal prompt in VS Code, type `dir`. This will show you all of the directories and files stored within your currently active directory.

  * You likely will see common Windows directories such as `Desktop` and `Documents` here.

Think about the location on your computer where it makes the most sense for you to store your files. Say, for example, that you want to create your root directory *inside* your Documents directory. We'll use that as our example.

2. From the command prompt, navigate into the `Documents` directory with the following command: `cd Documents`

3. Then enter the command `mkdir cit30900` at the command prompt.

4. Move into the newly-created directory with the command `cd cit30900`

5. You should see that your command prompt has changed and now includes the current directory. Your prompt will look something like `C:\Users\Username\Documents\cit30900>`

(devenv:windows:root_directory:gui)=
### Option 2: Create a Root Directory Using the Graphical User Interface

Think about the location on your computer where it makes the most sense for you to store your files. Say, for example, that you want to create your root directory *inside* your Documents directory. We'll use that as our example.

1. Using Windows Explorer, open your `Documents` folder.

2. Create a new folder named `cit30900` inside your `Documents` folder.

3. **Right-click** on your newly-created `cit30900` folder and choose "Show more options". Then choose "Open with Code" (the option with the VS Code icon).

This will open VS Code and set the active workspace to your `cit30900` directory. It *should* have also opened the VS Code panel and set the current working directory to your `cit30900` directory. (If the panel is not open, you can use the icon in the menu bar or press `Control+J`).

(devenv:windows:activate_venv_vscode)=
## Activate Your Virtual Environment in VS Code

You need to activate your virtual environment to ensure all of the Python packages you have downloaded will be available to you.

1. At the Terminal prompt **in VS Code** use the command to activate the virtual environment you created:

```
workon cit30900env
```

You should now see the name of your virtual environment appear prior to the command prompt in your VS Code terminal window.

```{image} ../img/windows-vscode-active-ve.png
:alt: An active virtual environment displayed at the command prompt in Visual Studio Code on the Mac
:align: center
:width: 300px
```

(devenv:windows:test_file)=
## Create a Test File

Regardless of the method you chose above, you should be ready to write and store code in VS Code. Create a test file to show the connection between the Terminal and your file editor in VS Code.

1. Ensure you are in your `cit30900` root directory.

When you installed VS Code, it added a special command that you can use to create and open a new file with a single command.

2. At the command prompt, type `code helloworld.py`.

You should see a file open in the file editor at the top of the VS Code window.

```{note}
If you are asked to trust the authors of any files, you should respond positively.
```

3. Enter a simple Python `print()` statement into your file:

```
print('Hello world!')
```

4. Save your file using the VS Code `File` menu, or by pressing `Control+S`

5. To see that the file is now saved in your local root directory, type the following at the command prompt: `ls`

You should see the file `helloworld.py` appear. As you add more directories and files, they will be displayed when you "list" (`ls`) your files.

6. Run your Python file with the following command in the VS Code terminal:

```
python helloworld.py
```

You should see your message output in the Terminal window.