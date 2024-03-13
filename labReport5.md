# Lab Report 3: Bugs and Commands

## Part 1: Debugging Scenario
### Screenshot showing a symptom and a description of a guess of what the failure-inducing input it

### Response from a TA asking a leading question or suggesting a command to try

### Screenshot/terminal output showing information from trying that and a clear description of the bug

### Information needed about the setup
* File & directory structure:
* Contents of each file before fixing the bug:
* Full command line run to trigger the bug:
* Description of what to edit to fix the bug

## Part 2: Reflection
*The most useful topic I learned from my lab experience during the second half of this quarter was how to use a script and take advantage of different commands to explore files and analyze specific text. Writing bash scripts helped me save a lot of time on my programming assignments for CSE 12 during testing, and the commands enabled me to get more information out of my code than I knew how to before. It was also fun to use vim to edit text in VSCode. 

### `find`: 4 command-line options used on files and directories from `./technical`
**Using `find -regex`**
\
*Example 1 command and output on `./technical/911report` directory
```

```
*What it's doing and why it's useful: It finds all path names in this `./technical/911report` directory containing the pattern chapter in the path name. It's useful for finding a path that you need for a file or directory.
\
\
*Example 2 command and output on `./technical/911report/chapter-1.txt` file.
```

```
*What it's doing and why it's useful: It just prints out the path to the file you use find -regex on. This could be useful for finding a specific file path from the working directory, but it's hard to see how it can be helpful when you already need the path for the command line.
\
\
**Using `find -mmin`**
\
*Example 1 command and output on `./technical/911report` directory
```

```
*What it's doing and why it's useful: It finds and prints out a path name list of all files and directories last modified in the last 60 minutes in the working directory. Since I just cloned the directory, all of these were modified within 60 minutes. This is useful for finding out what files were recently modified and could be used to double-check a deadline.
\
\
*Example 2 command and output on `./technical/911report/chapter-2.txt` file
```

```
*What it's doing and why it's useful: It just prints out the path name of the file you use find -mmin -60 on because `chapter-2.txt` was modified within the last 60 minutes when I created the directory. However, if I didn't modify it recently, it would probably not show anything. This could be useful for checking if that specific file was modified recently.
\
\
**Using `find -exec {} \;`**
\
*Example 1 command and output on `./technical/911report` directory
```

```
*What it's doing and why it's useful: It's printing all lines with the word "terrorist" in each file with path name "chapter-13" in the `./technical/911report` directory. This is useful for narrowing down searching code in a directory.
\
\
*Example 2 command and output on `./technical/911report/chapter-3.txt` file
```

```
*What it's doing and why it's useful: It's searching for all lines with "Hoover" on each file. Since the command was used on a file, `-exec grep {} \;` only accesses `chapter-3.txt`. This is useful for finding specific lines in a file, but it's not very necessary when we can use grep.
\
\
**Using `find -maxdepth`**
\
*Example 1 command and output on `./technical` directory
```

```
*What it's doing and why it's useful: It finds all directories, but limits the depth of searches to 2 directories descended. This is useful for limiting your search of all directories if there are too many directories within the one you're looking at.
\
\
*Example 2 command and output
```

```
*What it's doing and why it's useful: It's just printing out the file I'm using find on. Since I'm not using the command on a directory, it doesn't realy matter what the maxdepth is because there are no directories within a file. This is not really useful I think.
\
\
**Sources**
[Red Hat] (https://www.redhat.com/sysadmin/linux-find-command)
[IBM] (https://www.ibm.com/docs/pl/aix/7.1?topic=f-find-command)
