# PFI Github Introduction
This is a repo to demonstrate how to set up github with Eclipse and IntelliJ for MED2 Programming For Interaction (Programmering af Interaktive Systemer)

## Setting up your Git workspace

### Git Client
I recommend both having a command-line and GUI interface for working with Git.
* Git can be downloaded from https://git-scm.com/. This gives you a basic GUI client and a Git Bash, a powerful Command line tool for git.
    * I recommend **NOT** using vim, but chosing a different text editor. Personally I would recommend [Notepad++](https://notepad-plus-plus.org/) or [VS Code](https://code.visualstudio.com/) though any fast plain text editor is good
* In adition to Git, you will want a git client. 
    * [Github Desktop](https://desktop.github.com/) is a simple solution, but again I would recommend against it, as it is lacking in features. 
    * [SourceTree](https://www.sourcetreeapp.com/) is better, but needs to be set up initially with BitBucket and an Attlassian account, and then integrated.
    * [GitKraken](https://www.gitkraken.com/) is a good client. However, you need a paid subscription in order to use private repositories. Since this feature recently became free on Github, you may want to use it. If you do, then you need to look elsewhere than GitKraken
    * [**Fork**](https://git-fork.com/) is a feature rich client with a simple interface. This gets my recommendation, and all examples will be using this client.
    
### Setting up a Repository
You can create repositories through your command line, your Git Client, or on Github. For simplicity sake, I recommend creating the repository on Github first.

#### Create Repository Github
1. Create a new repository, and give it a short but descriptive name.
    * I like to have a `README.md` file for documentation, though it is not necessary.
    * You can find a premade Java gitignore, but this doesn't have everything that you want.
2. Clone Your project from Github to your computer.
    * Click "Clone or Download" on your repository's home page, and copy the link (e.g. `https://github.com/EoinRaff/PFS_Github_Introduction.git`)
3. Use either your command line or client to clone the repository.

##### (a) Clone via Command Line
1. Open your command line and navigate to the directory where you want to store your projects
    * If using git bash, you can (in windows, at least) navigate to this folder in the explorer, right-click and select "Git Bash here"
2. Use the `git clone` command followed by the address of you git repo to clone it (e.g. `$ git clone https://github.com/EoinRaff/PFS_Github_Introduction.git`)
    * Sometimes an error can occur here when pasting the address, so try typing it by hand
3. This will create a folder for your repository.

##### (b) Clone via Fork
1. In Fork, navigate to File > Clone...
2. If you have copied a url to your clipboard, it should appear automatically here. If not, then paste or type in the repository's address.
3. Select a location on your harddrive, and chose a name for the repo (I recommend not changing it from the name on Github)
4. Press the "Clone" button.

![alt text](https://github.com/EoinRaff/TA_Tutorial_Images/blob/master/PFI_Git_Intro/fork_clone.png "Cloning a project in Fork")


### Using a .gitignore file
Either add the `.gitignore` file from this repo, or edit your `.gitignore` to include the following lines:
```
# Eclipse
.classpath
.project
.settings/

# Intellij
.idea/
*.iml
*.iws

# Mac
.DS_Store

# Maven
log/
target/
```

As the name suggests, this file tells git what files to ignore.
Many files will be generated by your IDE (i.e. Eclipse or IntelliJ) or by Java when comiling and running your projects. 
These files do not need to be tracked by Git, as they will be automatically generated if they cannot be found.
As such, in order to keep your repository small and tidy, we ignore these files.
Likewise you may want to add files such as .png, .mp4 etc. if you have large texture or audio files, as they may be too large to upload to Github. 
* Git LFS exists for handling Large Files, though this has a tight storage limit on the free plan, and is somewhat complicated to manage. I will not go into it here, but it is worth knowing that it exists if you need it.

### Create a new project from your IDE
Wheter using Eclipse or IntelliJ, you create a new project as normal. The important step is to chose your repository as the containing folder, rather than the default suggestion.

If you have updated your .gitignore file, then all the IDE specific files will be ignored, and gihub will only track changes in the `src` folder (or other folders you create). 
This means that only the java classes that **you** create will be tracked. IDE specific files will remain on your computer, but will not be stored on github. 

Now if you are working with people using different IDEs, they can all work on the same `\src` folder and `.java` files, without having to have `.project` (eclipse) or `.idea` (intellij) files that they do not need.

## Git Workflow
```
Under Construction
1. How to use Fork
2. Git Flow (https://datasift.github.io/gitflow/IntroducingGitFlow.html)
```
