
## Basic linux commands

### Navigating your directeries


* show current working directory
```
pwd
```

* return or call your home directory
```
cd
```

* nativigate forward
```
cd dir (where dir = directory name with '/' dividing each subseqent folder)
```


* navigate backward

*note: repeat ../ for each folder preceeding*
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

* start, read, and edit a file

*note: nano is a default UI from commmand line to read and write, though limited in its ease of use*
*you will be promted upon exiting nano to save your file contents, if approved the filename will now exist in your directory*
```
nano filename
```

* read the file

*note: opens the whole file on command line*
```
cat filename
```

* read the start of a file

*here we are using a pipe '|' to call in the next command 'head -10' to read only the first 10 lines, you can change the number of lines as you see fit*
```
cat filename | head -10
```

* read the end of a file

*same as obve but using 'tail' to call lines from the end of a file
```
cat filename | tail -10
```

### Move files around

* copy the file
```
cp dir/filename newdir
```

* move the file (same a the 'cut' command on PC, file is not longer at original location)
```
mv dir/filename newdir
```

* delete a **file**
```
rm filename
```

* delete a **directory** (CAUTION: including EVERYTHING in it!)

*note: -r means recursive, all contents within the dir are called for deletion*
```
rm -r dir
```
