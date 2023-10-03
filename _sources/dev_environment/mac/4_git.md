# Establish a Root Directory and Install Git on MacOS

Git is source control management software that allows you to manage, back up, and collaborate while you are doing development work. Git should be installed automatically with MacOS, but it's often outdated. You'll use Homebrew to install the latest version of Git.

(devenv:mac:install_git)=
## Use Homebrew to Install Git
1. Open a Terminal on your computer
2. Use the following command to install Git:

```
brew install git
```

(devenv:mac:configure_git)=
## Configure Git on MacOS

Configure Git so it can automatically add your user details to the commits you will make to your repositories. 

1. Input the following commands on the MacOS Terminal command line, replacing the information as needed with your personal details.

```
git config --global user.name "Your Name"
```

You will *not* see any kind of feedback from the command prompt after you issue this command.

2. Use your school email address here (@iupui.edu or @iu.edu):

```
git config --global user.email "youremail@iu.edu"
```

Again, the command prompt will be empty after this command.