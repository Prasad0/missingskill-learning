# Linux

### History

* 1970 - Bell lab created system called Unix and started selling to different compaines and it was paid. It was the first OS.

* 1977 - Lots of companies started using Unix one of them was Berkeley university. But because it was costly and due to licencsing issue. Some reseacher from Berkeley and Ex-employee created a new system called BSD/Unix. It was developed by the Computer Systems Research Group (CSRG). This was cheaper than Unix.

* 1980 - 1985 - Richard stallman wanted to create his free Operating System. He started GNU project with goal to create same as UNIX OS. He also started Free Software foundation (FSF)

* 1987 - 1990 - Development of BSD was haulted because Bell lab put a legal deformation that BSD has stollen their code.

* 1990 - Linus Torvald created a kernal and made it available for free

* 1991 - Linus Torvald and Richard stallman both Formed GNU/Linux. Now anyone can get their own Operating System.

### Linux

1. Linux is a kernal.
1. Kernal - that communicate with computer hardware and software.
1. Linux was released under GNU general public license (GPL) means anyone can run, study, modify software.
1. In linux everything is a file.

### Popular Distribution

* GNU/Linux
* Debain
    * Ubuntu
* Redhat
    * Fedora
    * CentOs
    * Mint


### Commands :-

| Sr no | commands | flags | Description |
|-------|----------|-------|-------------|
| 1     | ls    |   | list all the file and floder pwd|
|       |          | -l | list all the file in distructive way |
|       |          | -h |human readable format |
|       |          | -t |sorted by modification date (recently created first) |
|       |          | -r |sorted by modification date (older file first) |
|       |          | -F |Can visually check it a file or folder |
|       |          | -a | will display all the hidden file and folder |
| 2     | cd       | | will take you to home folder|
|       | cd -      |  | holds the last position of the file |
|       | cd ~     |  | will take you to users home directories |
|       | cd ..      |  | will take you to previous folder |
|       | cd /     |  | will take you to root directory |
|3      | cp     |  | copy file from one location to another |
|       | cp     | -rf | will recursively copy file and folder |
|4 | tail -100f filename | | will print last 100 line and will keep on watching changes|
|5| cat || show entire file in terminal|
|| | > | to write a file|
|| | >> | to modify a file|
|6|less |  | similar to cat but prints command page wise (less gives more data)|
|7|more |  | similar to less (more gives less data)|
|8|echo |  | Print text or path on terminal |
|9|top |  | Gives all system level information (e.g ram used, application consuming memory) |
|10|ps -ef |  | list down all the application running in system |
|11|touch |  | Use to create new file  |
|12|ping |  | To check the connectivity with outside world |
|13|ifconfig |  | use to check IP or identify your IP (in windows we use ipconfig) |
|14|ssh |  | to access the remote server |
|15|mkdir |  | Make directory in pwd |
|16|rmdir |  | remove directory (it remove only if its empty directory) |
|17|rm |  | remove the file but not directory|
|| | -rf | remove the directory and file recursively |
|| |*  | will delete all the files |
|18|mv  |  | To move the file or folder from one location to another (cut paste type). Move can also be use to rename file or folder |
|19|pwd  |  | Print working directory |
|20|who  |  | Print number of user login to the system |
|21|whoami  |  | Tells who is current login user |
|22|history  |  | Display the number of command ran |
|23|which  |  | gives location where the application or command names are installed |
|24|wget  |  | fetch the getter from website and save in json format |
|25|exist  |  | If you are logged in to server you will be logged out / or - to exist the terminal |


### File System:- 

 `Whenever we start linux or *nix machine it looks for /boot folder -> this is where kernal config is store or kernal is located`


* $- normal user
* #- Root user

|Directory| files stored|
|---------|-------------|
|/| root file system|
|/boot | System kernal is stored|
|/bin| Binary files are stored here (Basically command are store here)
|/sbin | System Binary (it's related to system or kernal and used by sys admin)|
|/home|User Data is stored here|
|/var| Variable file (e.g log file)|
|/usr| user system resource (All software are stored here)|
|/root| its a root folder. home directory of root user only privilege or su user can login to root folder |
|/tmp | Temporary files are stored here|
|/etc |System configuration are stored here|
|/lib |System libraries are store here|
|/mnt | This are for CD roms|
|/dev | external device are attached here|
|/opt | contains sub directories for optional package|















