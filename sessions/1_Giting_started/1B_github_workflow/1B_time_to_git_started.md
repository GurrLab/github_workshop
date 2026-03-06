# Before we '*Git*' going..

___

**1)** Tasks completed before the workshop, if you have not completed these please do

- Install git on your computer [here](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgit-scm.com%2Finstall%2Fwindows&data=05|02|samuel.gurr@oregonstate.edu|d4d7777645d8408b6f0d08de74ccc5f1|ce6d05e13c5e4d6287a84c4a2713c113|0|0|639076619996014391|Unknown|TWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D|0|||&sdata=WHxcGZeNBbo6XsfH%2FeabxItUhpZsdF4Cy1xU5GeZX8Q%3D&reserved=0)

- sign up on github [here](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2F&data=05|02|samuel.gurr@oregonstate.edu|d4d7777645d8408b6f0d08de74ccc5f1|ce6d05e13c5e4d6287a84c4a2713c113|0|0|639076619996050849|Unknown|TWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D|0|||&sdata=KyQeYek5F1X%2FKqZcHtXuM7740gFuDDUBY6RZtcpuAq4%3D&reserved=0) 

- Read '1. Automated Version Control' [here](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Fswcarpentry.github.io%2Fgit-novice%2F01-basics.html&data=05|02|samuel.gurr@oregonstate.edu|d4d7777645d8408b6f0d08de74ccc5f1|ce6d05e13c5e4d6287a84c4a2713c113|0|0|639076619996079772|Unknown|TWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D|0|||&sdata=w97mq3MB5bPdzsJv%2FTMlGcfPi%2B%2BOctZeYoDuUFXrKrQ%3D&reserved=0)

**2)** Follow GurrLab on github! 

* this enables me to easily grab your username to make you a collaborator for the workshop
* ..and following is fun

**3)** Learn basic bash commands in the git bash command line [here](https://github.com/GurrLab/github_workshop/blob/main/sessions/1_Giting_started/1A_linux_commands/1A_basic_linux_commands.md)

# '*Git*' ready...

___

 **Topics for this workshop**:

- **Clone** the workshop repository to your personal computer, each of you have collaborator writing access
  - learn how the clone process differs if you are or are not a collaborator on the repository

- Understand core fundaments of github workflow **pull-add-commit-push-pull**

- Create **add a file** and **push** it to the remote repository

- **Pull** updates as your peers add their files to the main directory

- Discuss **merge conflicts** and best practices to avoid and remedy them

* initiate team-based version control using our collaborative 'github_workshop' repo

	- use basic linux commands to navigate your computer, create files, edit them, etc.
- use a handful of git commands to clone, edit, and add to the collaborative 'github_workshop' repository
* time permitting, make your own repository on your page

# '*Git*' set... GO!
steps supplemented with color-coded <span style="color:red">bash</span> and <span style="color:green">git</span> commands

#### objectives:

* link a remote repository to your personal computer 
* understand the value of github as a collaborative team
* use <span style="color:red">bash</span> commands to view, open, and edit files

  * use default text editors from command line <span style="color:red">nano</span>, <span style="color:red">vim</span>

  * (optional) create an alias shortcut to open an alternative text editor of your choice

  * create a new file save it in the output folder on github_workshop
* use a sequential workflow of <span style="color:green">git</span> commands

  * <span style="color:green">git pull</span> to integrate changes on the main branch that you do not have on your computer

  * <span style="color:green">git status</span> to view changes you made

  * <span style="color:green">git add</span> to add your changes to the queue

  * <span style="color:green">git commit -m " "</span> to establish a record of your changes

  * <span style="color:green">git push</span> to integrate your changes to the main repository

## 1) *<span style="color:green">git clone</span>* the [github_workshop](https://github.com/GurrLab/github_workshop) repo 

**1.1.**) Open git on your computer

**1.2.)** Use <span style="color:red">bash</span> commands ([tutorial](https://github.com/GurrLab/github_workshop/blob/main/sessions/1_Giting_started/1A_linux_commands/1A_basic_linux_commands.md)) to navigate to a directory where you want the 'github_workshop' repository to live. You are now ready to <span style="color:green">git</span> the repository. Skip to 'c.' if you completed the bash tutorial

**Note**: the 'github_workshop' repository is already active and on github. You can establish a new repository from command line (example tutorial [here](https://kbroman.org/github_tutorial/pages/init.html)) though we will not do this today

* <span style="color:red">cd</span> to return or call your home directory

* <span style="color:red">ls</span> to read the directory listing (what is in the current directory?)

* copy the file using <span style="color:red">cp</span>

* move file using <span style="color:red">mv</span> 

* CAUTION: delete a **file** using <span style="color:red">rm</span>

* CAUTION: delete a **directory**  using <span style="color:red">rm -r</span>
  - NOTE:  -r means recursive, all contents within the directory are deleted 


* The asterisk is a powerful tool <span style="color:red">*</span> - when placed before or after a common filename string, its purpose is to call all content with that string
  * example: you want to move only year 2022 files to a different folder, your folder contains the following:
    * 2022_temp_1.xls
    * 2022_salinity_2.xlsx
    * 2022_pH_5.csv
    * 2021_temp_2.xlsx


```
mv 2022* <dir destination>
```

**1.3.)** Open the online page for the repository [github_workshop](https://github.com/GurrLab/github_workshop). Remember, you are a collaborator with writing permissions.

**1.4.)** click on the **green box that says 'Code'**. TCopy the HTTPS option for cloning the repository https://github.com/GurrLab/github_workshop.git.

**1.5.)** in your git window, clone the repository using <span style="color:green">git clone</span> as the following command

* you will see a it load from your git command line, should reach 100% quickly

```
git clone https://github.com/GurrLab/github_workshop.git
```

* use <span style="color:red">ls</span> to check the folder contents 

  ```
  ls
  ```

### Great work!

You 'git' the power and now have the current head directory of github_workshop on your laptop!

Importantly, each of you are collaborators with editing rights

A large team such as this workshop, each master rights can easily spiral to data conflicts when one version is behind/past another.
Without use of best practices, issues worsen as teams grow and become more productive. 

Seems counter-intuitive right? 

Working in this informal setting with non-critical files (within the github_workshop repository) allows us to troubleshoot and build confidence as a team!

## 2) Workflow - *<span style="color:green"> git pull, status, add, commit, push</span>*, oh my!

**2.1.**)  navigate to the **output** folder located at github_workshop/sessions/1_Giting_started/1B_github_workflow/**output**

* you will require bash commands <span style="color:red">cd</span> and <span style="color:red">ls</span> to navigate and ensure you are in the right place

**2.2.**)  use a text editor to create a markdown file called <LastnameYYYY.md>. Ex: Gurr2026.md

Options for text editors: 

* **<span style="color:red">nano</span>** 
  * a default test shell from command line to read and write, though limited in its ease of use. Ex: only arrow keys to navigate, no shortcuts such as Cntrl+C to copy will function

```
nano LastnameYYYY.md
```

* **<span style="color:red">vim</span>** 
  * another stock text shell, even more cumbersome than nano.
  * press ESC to open the command mode. press :q! and ENTER to quit

```
vim LastnameYYYY.md
```

* **lets call an easier user interface to work in shall we!**

  * below we will navigate to our home directory and edit our .bashrc file.  This file contains editable configurations for the use to interact with terminal


  * navigate home

    ```
    cd ~/
    ```

  * open .bachrc using nano

    ```
    nano .bashrc
    ```

  * the GNU will open, looks like command line window with option band below.

  * click with your cursor in the empty space, add the text below to make an **shortcut** as an **'alias'** to **notepad.exe** which is a default text editor on our PCs

    ```
    alias note='C:/Windows/System32/notepad.exe'
    ```

  * we now have a shortcut to use in terminal/git to open notepad as opposed to the clunky nano and vims!

  * close git and reopen to integrate this changes

  * type note to open notepad


```
note LastnameYYYY.md
```

**2.3.**) Use <span style="color:green">git pull</span> to integrate changes on the remote main branch 

```
git pull
```

* if there are no changes, it will say it is up to date

	- Note: this is the step where merge conflicts may arise, we can work on this in future meetings

**2.4.**) Use <span style="color:green">git status</span> to view changes you made. This should show the LastnameYYYY.md in red to indicate is a pending edit that has not been added

```
git status
```

**2.5.**) Use <span style="color:green">git add</span> to add your changes to the queue.

```
git add <dir>/LastnameYYYY.md
```

* you can also use git add ./ to add all changed in a given directory

**2.6.**) Use <span style="color:green">git status</span> again. You will now see LastnameYYYY.md is green because you verified it was a change you want to add

```
git status
```

**2.7.**) Use <span style="color:green">git commit</span> with <span style="color:green">-m</span> to establish a record of your changes

```
git commit -m "a message here for your record, requires quotes!"
```

*  rerun git status it will tell you there is nothing to add, a commit is a step above meaning that the changes are established to move forward

**2.8.**) Use <span style="color:green">git push</span> to integrate your changes to the repository

* <span style="color:green">origin main</span> == to the main repository

* <span style="color:green">origin master</span> == older git repos are called 'master', however ours is 'main' so do not worry

```
git push origin main
```

# Celebrate, you 'git' it!

**your changes to teamwork are now integrated in the main repository.** [Check it out on github](https://github.com/SamGurr/RClub)
