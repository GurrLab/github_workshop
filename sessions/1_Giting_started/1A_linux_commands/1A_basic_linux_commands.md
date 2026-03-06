# Basic linux (bash) commands

### Objective

Use syntax on the git bash command line to move around in your subfolders, view contents, create folders, start files, rename files, delete files, etc. 

### Before getting started...

**1)** Hop into your file explorer (windows) or finder (mac) and create a folder within Documents 

* example: create a folder **linux_test** located in your Documents, so the full directory is Documents/**linux_test**

**2)** Open a text editor such as Notepad (windows) or TextEdit (mac) and create a file, save it within the subfolder you created in #1 

**3)** Open Git Bash

### Navigating your directories in git bash command line

**Fun fact**: the language **bash** is the default shell to communicate with Linux systems. You will learn some basic bash code in this tutorial!


* show current working directory

*If I were to execute a command, where am I on my computer?*

```
pwd
```

* return to or call your home directory

```
cd
```

* navigate forward
```
cd dir (where dir = directory name with '/' dividing each successive folder)
```


* navigate backward

*note: repeat ../ for each folder preceding your current*

```
cd ../
```

* directory listing (what is in the current directory?)
```
ls
```

* make a directory
```
mkdir dir (dir is the directory name)
```


### Examine and edit file contents

* navigate to the subfolder you made at the start of this tutorial 
  * example: **linux_test**


```
cd # navigate back to your home directory (if you went elsewhere)

cd Documents/linux_test # navigate to the folder
```

* start, read, and edit a file

**Note**: nano is a default UI from command line to read and write, though limited in its ease of use
you will be prompted upon exiting nano to save your file content, and confirm the filename. If approved the filename will now exist in your directory

	* create a file called filename (of course, call it whatever you like!)

```
nano filename
```

* add content on >20 lines, can be whatever floats your boat

```
Hello
I 
Was
told
to 
write
on
many
lines
of
this
nano
thing
okay
im
done
now
bye
bye
```

* exit and save using the prompts on the bottom of the nano interface

* read the file

*note: opens the whole file on command line*

```
cat filename
```

* read the start of a file

*here we are using a pipe '|' to call in the next command 'head -10' to read only the first 10 lines, you can change the number of lines as you see fit*
```
cat filename | head -5
```

* read the end of a file

*same as above but using 'tail' to call lines from the end of a file*

```
cat filename | tail -5
```

### Move files around

**CAUTION** : some of this code will rename and delete files and contents

* copy the file
```
cp dir/filename newdir
```

* move the file (same a the 'cut' command on PC, file is no longer at original location)
```
mv dir/filename newdir
```

* delete a file
```
rm filename
```

* delete a **directory** (CAUTION: including EVERYTHING in it!)

*note: -r means recursive, all contents within the dir are called for deletion*
```
rm -r dir
```

### Let's use what we learned to delete what we built! 

**1)** Move the text file you made back one directory 

**2)** Navigate back one directory 

**3)** List the directory contents to see if the file is there

**4)** Move the file back to the original subdirectory that you started for this tutorial (i.e. linux_test)

**5)** Carefully (!!!), permanently delete the subdirectory you started for this tutorial

* note, to call this directory you need to be positioned behind it

