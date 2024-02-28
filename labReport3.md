# Lab Report 3: Bugs and Commands

## Part 1: Bugs

**Using `/add-message` Example 1**
![Image](2Example1.png)


**Using `/add-message` Example 2**
![Image](2Example2.png)


## Part 2: Researching Commands

### `find`: 4 coommand-line options used on files and directories from `./technical`
**Using `find -regex`**
Example 1 command and output on `./technical/911report` directory
```
Cyrene@charless-MacBook-Pro technical % find 911report -regex ".*chapter.*"
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
*What it's doing and why it's useful: It finds all path names in this `./technical/911report` directory containing the pattern chapter in the path name. It's useful for finding a path that you need for a file or directory.
Example 2 command and output on `./technical/911report/chapter-1.txt` file.
```
Cyrene@charless-MacBook-Pro technical % find 911report/chapter-1.txt -regex ".*chapter.*"
911report/chapter-1.txt
```
*What it's doing and why it's useful: It just prints out the path to the file you use find -regex on. This could be useful for finding a specific file path from the working directory, but it's hard to see how it can be helpful when you already need the path for the command line.
**Using `find -mmin`**
Example 1 command and output on `./technical/911report` directory
```
Cyrene@charless-MacBook-Pro technical % find 911report -mmin -60
911report
911report/chapter-13.4.txt
911report/chapter-13.5.txt
911report/chapter-13.1.txt
911report/chapter-13.2.txt
911report/chapter-13.3.txt
911report/chapter-3.txt
911report/chapter-2.txt
911report/chapter-1.txt
911report/chapter-5.txt
911report/chapter-6.txt
911report/chapter-7.txt
911report/chapter-9.txt
911report/chapter-8.txt
911report/preface.txt
911report/chapter-12.txt
911report/chapter-10.txt
911report/chapter-11.txt
```
*What it's doing and why it's useful: It finds and prints out a path name list of all files and directories last modified in the last 60 minutes in the working directory. Since I just cloned the directory, all of these were modified within 60 minutes. This is useful for finding out what files were recently modified and could be used to double-check a deadline.
Example 2 command and output on `./technical/911report/chapter-2.txt` file
```
Cyrene@charless-MacBook-Pro technical % find 911report/chapter-2.txt -mmin -60
911report/chapter-2.txt
```
*What it's doing and why it's useful: It just prints out the path name of the file you use find -mmin -60 on because `chapter-2.txt` was modified within the last 60 minutes when I created the directory. However, if I didn't modify it recently, it would probably not show anything. This could be useful for checking if that specific file was modified recently.
**Using `find -size`**
Example 1 command and output
```

```
*What it's doing and why it's useful: It's evaluating if the file 
Example 2 command and output
```

```
*What it's doing and why it's useful:
**Using `find -newer`**
Example 1 command and output
```

```
*What it's doing and why it's useful:
Example 2 command and output
```

```
*What it's doing and why it's useful:

**Source:**
