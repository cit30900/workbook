# Install Homebrew
Homebrew is a package manager for Mac computers. It helps you install, update, and uninstall system software.

1. Open a new Terminal window (or use a window that is open)
2. Copy and paste the following command into the Terminal window

*(Copy and paste this ENTIRE line - it is word-wrapping in the documentation, but it is a single command.)*

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

3. Input your administrative password when asked

```{important}
After installing Homebrew, **READ THE MESSAGES PROVIDED**. The installer *may* give you two commands that you should copy and paste into the Terminal window.

The first command will start with:
```(echo; echo 'eval "$(/usr/local/bin/brew shellenv)"') >> ...```

The second will look like:
```eval "$(/usr/local/bin/brew shellenv)"```

The specific commands will differ based on your individual computer. Please read the feedback and execute the commands provided.
```