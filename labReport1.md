# Lab Report 1

## Commands with *no* arguments

**`cd`**
![Image](cdNoArg2.png)
* Working directory: `/home/lecture1/messages`
* The command `cd` causes the terminal to change directories and go back to the root directory `/home`. When `cd ..` is used, the terminal goes out one directory to `/lecture1`.
* This is not an error.

**`ls`**
![Image](lsNoArg.png)
* Working directory: `/home`
* The command prints out `lecture1` because `ls` functions to list out all files and folders in a directory. It assumes that the argument is the current working directory, so it only prints out 1 folder, which is directy under `/home` in the filesystem.
* This is not an error.

**`cat`**
![Image](catNoArg.png)
* Working directory: `/home`
* The command changes the terminal to be in standard text, instead of allowing the programmer to give commands. Since there is no argument, `cat` assumes that it should print input directly from the terminal. 
* This is not an error.

## Commands with a path to a *directory* as an argument

**`cd lecture1/messages`**
![Image](cdDirectory.png)
* Working directory: `/home`
* The current working directory changes to `lecture1/messages` because cd follows the path given when both `lecture` and `messages` are folders, and `messages` is listed under `lecture1` in the filesystem.
* This is not an error.

**`ls messages`**
![Image](lsDirectory.png)
* Working directory: `/lecture1`
* The command prints out `en-us.txt  es-mx.txt  ja.txt  zh-cn.txt`, because they are all the files under the `/messages` folder in the filesystem. 
* This is not an error.

**`cat messages`**
![Image](catDirectory.png)
* Working directory: `/lecture1`
* The command prints out the output that messages is a directory, meaning that we need to use a file after cat to print out a file's contents.
* This is an error because `cat` cannot read the contents of a folder because a folder has no text or code content. It only contains other files in the filesystem.

## Commands with a path to a *file* as an argument

**`cd lecture1/Hello.java`**
![Image](cdFile.png)
* Working directory: `/home`
* The command prints out that `lecture1/Hello.java` is not a directory Hello.java is listed as a file under `/lecture1`.
* This is an error because `cd` was used on a file, not a folder, and the current working directory can only be used to change between folders.

**`ls messages/en-us.txt`**
![Image](lsFile.png)
* Working directory: `/lecture1`
* The terminal prints out `messages/en-us.txt` because the only file listed under en-us.txt is itself in the filesystem.
* This is not an error.

**`cat Hello.java`**
![Image](catFile.png)
* Working directory: `/lecture1`
* The command prints out all the code in the Hello.java file because its function is to show the contents of a file on the terminal.
* This is not an error.