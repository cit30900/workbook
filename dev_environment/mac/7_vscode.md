# Install Visual Studio Code

All demonstrations and videos this semester will use Visual Studio Code as the IDE (integrated development environment). I strongly urge you to use VS Code for your own development – it has Git integration, code highlighting and syntax, and a built-in terminal that will help you run your web applications locally.

`````{admonition} Pro Tip!
:class: tip

Visual Studio **Code** is a free, open-source code editor. It is different from the complete Visual Studio package.

You'll often see it referred to as "VS Code" or just "Code", but it should not be confused with Visual Studio.
`````

(devenv:mac:install_vscode)=
## Install Visual Studio Code

1. If you have not already, [download and install Visual Studio Code](https://code.visualstudio.com/download). Choose the `.zip` version for your processor type.

(devenv:mac:vscode_shell)=
## Add "code" Command to MacOS Shell

You will now set up a direct connection between MacOS' Terminal and Visual Studio Code by adding a special `code` command that you can run from the command line.

1. Open Visual Studio Code.
2. Press `command + shift + p` to open the command palette, then type "install code", and then click **Shell command: Install 'code' command in PATH**.
3. Restart your shell by typing the command `source/~.zshrc` into a MacOS Terminal window
4. In MacOS Terminal, type `code test.txt`.

This will create a file named `test.txt` in whatever the active directory was in your Terminal. Visual Studio Code should also launch and open the file, ready for you to start entering text.

You can delete the `test.txt` file, as we will not use it.