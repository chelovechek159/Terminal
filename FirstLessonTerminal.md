# The first part of the first HomeTask (Linux terminal (GitBash) commands)
___
### 1. View current location - *pwd*

>shows the path to the current folder

### 2. Create folder - *mkdir*
>you can create one or more folders with the mkdir command

	mkdir Terminal - 1 folder named Terminal
	mkdir folder1 folder2 folder3 - 3 folders
	mkdir -p fol1/fol2 - to create a folder inside a folder add -p
	
### 3. Go to folder - *cd* [path]
    cd downloads/films/fantasy - go to the fantasy folder
    cd .. - will return one level up - to the films folder
    cd - returns to home folder
	
### 4. Create 3 folders - *mkdir folder1 folder2 folder3*
### 5. Go to any folder - *cd folder1*
### 6. Create 5 files (3 txt, 2 json) - *touch*
 
5 files in one line:

	touch 1.txt 2.txt 3.txt 4.json 5.json

or each file separately:    

	touch 1.txt
	touch 2.txt
	...

### 7. Create 3 folders - *mkdir fold1 fold2 fold3*
### 8. List folder contents - *ls*  

command and options such as *-la* (lists all files and folders including hidden) and the path to the required folder.

	ls -la

result

		total 0
		drwxr-xr-x  10 yaroslav  staff  320 Apr 18 22:21 ./
		drwxr-xr-x  11 yaroslav  staff  352 Apr 18 22:20 ../
		-rw-r--r--   1 yaroslav  staff    0 Apr 18 22:21 1.txt
		-rw-r--r--   1 yaroslav  staff    0 Apr 18 22:21 2.txt
		-rw-r--r--   1 yaroslav  staff    0 Apr 18 22:21 3.txt
		-rw-r--r--   1 yaroslav  staff    0 Apr 18 22:21 4.json
		-rw-r--r--   1 yaroslav  staff    0 Apr 18 22:21 5.json
		drwxr-xr-x   2 yaroslav  staff   64 Apr 18 22:21 fold1/
		drwxr-xr-x   2 yaroslav  staff   64 Apr 18 22:21 fold2/
		drwxr-xr-x   2 yaroslav  staff   64 Apr 18 22:21 fold3/

### 9. Open any txt file - *cat*
	cat 2.txt
	
### 10. Write any text in file. - *cat > 1.txt*

>Entered any text
### 11. Save and exit. - Press keyboard shortcut *"control + C"*
### 12. Exit folder one level up - *cd ..*
### 13. Move any 2 files you created to any other folder. - *mv* 
	mv folder1/1.txt folder1/2.txt folder2 - moved 2 files at once to the folder2.

Additional functions:
    
    -f - replace file if it already exists;
    -i - ask if existing files need to be replaced;
    -n - do not replace existing files;
    -u - replace the file only if it has been changed;
    -v - display a list of processed files;
	
### 14. Copy any 2 files to any other folder. - *cp* 
	cp folder1/4.json folder1/5.json folder2 - copied 2 files to folder2.
### 15. Find file by name - find command
	find . -name "1.txt"

>	./folder2/1.txt
### 16. View the content in real time - *tail* 
command with an additional option -f (on macOS devices, some files are ignored) so use -F

	tail -F folder2/1.txt

result

        we
        fs
        d
        cs
        123
        456
        ^C⏎  to end the command, press the key combination "control + C"

### 17. Output the first few lines from a text file - *head*
>Print the first 7 lines 
	
	head -7 folder2/1.txt 
       
 result
       
    asd
    qw
    ewr
    erg
    er32
    r23
    r

### 18. Output the last few lines from a text file - *tail*
>Print the last 7 lines 

	tail -7 folder2/1.txt 
         
result

    cs
    123
    456
    789
    12381203929
    123
    Asda⏎    

### 19. View the contents of a long file *- less*

	less 1.txt

While viewing the text, the utility can be controlled using internal 
    commands by typing them on the computer keyboard. 
    The most commonly used ones are:

    h, H - help;
    Space, Ctrl+V, f, Ctrl+F - scroll the text one screen forward;
    Enter, Return, Ctrl+N, e, Ctrl+E, j, Ctrl+J — scroll text forward n lines, default n=1;
    y, ctrl+y, Ctrl+P, k, Ctrl+K — scroll text n lines back, n=1 by default;
    Ctrl+→ - scroll the text horizontally to the end of the line;
    Ctrl+← - scroll the text horizontally to the beginning of the line;
    :d - remove the current file from the list of files;
    Ctrl+G, :f - display basic information about the file;
    q, Q, :q, :Q, ZZ - exit(output).


### 20. display date and time - *date*
    date
    Tue Apr 18 22:32:16 +03 2023
    
 To output in a different format, you need to add + sign and additional functions
   
    date +%x_%X
    04/18/2023_22:32:28

    date +%F_%X
    2023-04-18_22:32:34

___
##TASK *
### *1. Send an http request to the server - *curl*  
you can use additional functions (to save the content -o; To fetch the headers of the URL -I; for a more detailed description -v etc.)

	curl http://162.55.220.72:5005/terminal-hw-request


### *2. Write a script that will automatically execute steps 3, 4, 5, 6, 7, 8, 13
I tried this method, I liked it the most.

	touch 1.sh - create new file (with or without .sh domain)
	vim 1.sh - entered commands; saved data and exited
	cat 1.sh - looked at the contents of the file, made sure that everything was saved

```
	#!/bin/bash
		cd folder1
			mkdir fold_1 fold_2 fold_3
					cd fold_2
				touch 11.txt 22.txt 33.txt 44.json 55.json
			mkdir f1 f2 f3
		ls -la 
```
    mv 11.txt 22.txt f1
    chmod u+x 1.sh 
In short, chmod +x following by a filename, usually a script, means that you make it executable. U - user.

	./1.sh 

result

    total 0
    drwxr-xr-x  10 yaroslav  staff  320 Apr 18 22:41 .
    drwxr-xr-x  11 yaroslav  staff  352 Apr 18 22:41 ..
    -rw-r--r--   1 yaroslav  staff    0 Apr 18 22:41 11.txt
    -rw-r--r--   1 yaroslav  staff    0 Apr 18 22:41 22.txt
    -rw-r--r--   1 yaroslav  staff    0 Apr 18 22:41 33.txt
    -rw-r--r--   1 yaroslav  staff    0 Apr 18 22:41 44.json
    -rw-r--r--   1 yaroslav  staff    0 Apr 18 22:41 55.json
    drwxr-xr-x   2 yaroslav  staff   64 Apr 18 22:41 f1
    drwxr-xr-x   2 yaroslav  staff   64 Apr 18 22:41 f2
    drwxr-xr-x   2 yaroslav  staff   64 Apr 18 22:41 f3
    
