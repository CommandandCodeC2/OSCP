
| Level | Password |
| :--- | :---: |
| 0| bandit0 |
| 1| ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If |
| 2| 263JGJPfgU6LtdEvgfWU1XP5yac29mFx |
| 3| MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx |
| 4| 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ |
| 5| 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw |
| 6| HWasnPhtq9AVKe0dmk45nxy20cvUa6EG |
| 7| morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj |
| 8| dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc |
| 9| 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM |
| 10| |
| 11| |
| 12| |
| 13| |
| 14| |
| 15| |
| 16| |
| 17| |
| 18| |
| 19| |
| 20| |
| 21| |
| 22| |
| 23| |
| 24| |
| 25| |
| 26| |
| 27| |
| 28| |
| 29| |
| 30| |
| 31| |
| 32| |
| 33| |


### Level 0

To complete level 0 you must SSH into then bandit training area using the command ```ssh bandit0@bandit.labs.overthewire.org -p 2220``` . Once inside you will read the contents of the readme file located in the home directory using the command ```nano readme```

### Level 1

To complete level 1 you must SSH into then bandit training area using the command ```ssh bandit1@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem . Once inside you will read the contents of the "-" file located in the home directory using the command ```nano ./-```

### Level 2

To complete level 2 you must SSH into then bandit training area using the command ```ssh bandit2@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem . Once inside you will read the contents of the " --spaces in this filename--" file located in the home directory using the command ```nano ./--spaces\ in\ this\ filename--```

### Level 3

To complete level 3 you must SSH into then bandit training area using the command ```ssh bandit3@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem . Once inside you will read find the password by running the command ```nano inhere/...Hiding-From-You```

### Level 4

To complete level 4 you must SSH into then bandit training area using the command ```ssh bandit4@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem . Once inside you will read find the password by running the command ```nano inhere/...Hiding-From-You```

### Level 5

To complete level 5 you must SSH into then bandit training area using the command ```ssh bandit5@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem. Once inside you will find need to locate the file in the inhere directory. In order to find the file you need to run the command ``` find . -type f -size 1033c ! -executable -exec file {} + | grep -w text ``` 

```find . ``` starts a search in the current directory (.) and everything beneath it, recursively.
``` -type f```  only matches to files and not directories 
``` - size 1033c ```: looks for files with 1033 bytes 
``` ! -executable -exec ``` Not executable files
``` file {} + ```: inspects the file to pull out the content types
``` | grep -w text``` filters out only file that are text types

### Level 6

To complete level 6 you must SSH into then bandit training area using the command ```ssh bandit6@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem. Once inside you will find need to locate the file on the server that containse the password. In order to find the file you need to run the command ``` find / -user bandit7 -size 33c -group bandit6  2>/dev/null ``` 

```find / ``` starts a search in the root directory (/) and everything beneath it, recursively.
``` -user bandit7```  only matches files that are owned by bandit7
``` - size 33c ```: looks for files with 33 bytes
```  -group bandit6 ```only matches files that are owned by the group bandit6
``` 2>/dev/null ```:  Sends all routine errors (2) to the /dev/null file (a black hole)

### Level 7

To complete level 7 you must SSH into then bandit training area using the command ```ssh bandit7@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem. Once inside you will find need to locate the file data.txt in the home directory. you will the run the command ``` grep millionth data.txt```.


### Level 8

To complete level 7 you must SSH into then bandit training area using the command ```ssh bandit8@bandit.labs.overthewire.org -p 2220``` and the password from the previous problem. Once inside you will need to locate the file data.txt in the home directory. you will the run the command ```.sort data.txt | uniq -c ```









