# 0x16. C - Simple Shell Project
## Building a simple UNIX command interpreter using "C" language.
**Requirements**
+ Allowed editors: vi, vim, emacs.
+ All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89.
+ All your files should end with a new line.
+ A README.md file, at the root of the folder of the project is mandatory.
+ Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
+ Your shell should not have any memory leaks.
+ No more than 5 functions per file.
+ All your header files should be include guarded
+ Use system calls only when you need to (why?)
+ Write a README with the description of your project.
+ You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository. Format, see Docker.

## Output 
+ Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.

+ The only difference is when you print an error, the name of the program must be equivalent to your argv[0] (See below):


## Code

Example of error `output` in  `sh`

    $ echo "qwerty" | /bin/sh
    /bin/sh: 1: qwerty: not found
    $ echo "qwerty" | /bin/../bin/sh
    /bin/../bin/sh: 1: qwerty: not found  
    $

Example of error `output` in  `hsh`

    $ echo "qwerty" | ./hsh
    ./hsh: 1: qwerty: not found
    $ echo "qwerty" | /./././hsh
    ./././hsh: 1: qwerty: not found  
    $



## List of allowed functions and system calls

+ `access` (man 2 access)
+ `chdir`   (man 2 chdir)
+ `close` (man 2 close)
+ `closedir` (man 3 closedir)
+ `execve` (man 2 execve)
+ `exit` (man 3 exit)
+ `_exit` (man 2 _exit)
+ `fflush` (man 3 fflush)
+ `fork` (man 2 fork)
+ `free` (man 3 free)
+ `getcwd` (man 3 getcwd)
+ `getline` (man 3 getline)
+ `getpid` (man 2 getpid)
+ `isatty` (man 3 isatty)
+ `kill` (man 2 kill)
+ `malloc` (man 3 malloc)
+ `open` (man 2 open)
+ `opendir` (man 3 opendir)
+ `perror` (man 3 perror)
+ `read` (man 2 read)
+ `readdir` (man 3 readdir)
+ `signal` (man 2 signal)
+ `stat` (__xstat) (man 2 stat)
+ `lstat` (__lxstat) (man 2 lstat)
+ `fstat` (__fxstat) (man 2 fstat)
+ `strtok` (man 3 strtok)
+ `wait` (man 2 wait)
+ `waitpid` (man 2 waitpid)
+ `wait3` (man 2 wait3)
+ `wait4` (man 2 wait4)
+ `write` (man 2 write)

### Compilation

```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```
## Testing
##### Your shell should work like this in interactive mode:
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```
##### But also in non-interactive mode:
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```
#### GitHub repository: `simple_shell`
## Tasks

| Task| Description |
| ------ | ----------- |
| **0. Betty would be proud** | Write a beautiful code that passes the Betty checks.|
|        |             |
| **1. Simple shell 0.1** |  Write a UNIX command line interpreter.Usage: `simple_shell`
|        |            |
| **2. Simple shell 0.2**| Handle command lines with arguments.|
|        |            |
| **3. Simple shell 0.3** | Handle the PATH fork must not be called if the command doesn’t exist |
|        |            |
|**4. Simple shell 0.4**| Implement the `exit` built-in, that exits the shell. Usage: `exit`. You don’t have to handle any argument to the built-in `exit`.|
| | |
|**5. Simple shell 1.0**| Implement the env built-in, that prints the current environment.|
| | |
|**6. Simple shell 0.1.1**| Write your own `getline` function. Use a buffer to read many chars at once and call the least possible the `read` system call. You will need to use static variables. You are not allowed to use `getline`.|
| | |
|**7. Simple shell 0.2.1**| You are not allowed to use strtok.|
| | |
|**8. Simple shell 0.4.1**| handle arguments for the built-in `exit`. Usage: `exit status`, where `status` is an integer used to exit the shell.|
| | |
|**9. setenv, unsetenv**| Implement the setenv and unsetenv builtin commands.|
| | |
|**10. cd**| Implement the builtin command cd:|
| | |
|**11. ;**| Handle the commands separator ; |
| | |
|**12.&& and OR.**| Handle the && and OR shell logical operators.|
| | |
|**13. alias.**| Implement the alias builtin command|
| | |
|**14. Variables**| Handle variables replacement. Handle the `$?` variable. Handle the `$$` variable.|
| | |
|**15. Comments**| Handle comments `(#)`. |
| | |
|**16. File as input**| Usage: `simple_shell [filename]`.Your shell can take a file as a command line argument. The file contains all the commands that your shell should run before exiting. The file should contain one command per line. In this mode, the shell should not print a prompt and should not read from `stdin.`|

This project was carried out by Oti-owom Emmanuel Ubani with email:(ezeogouba@gmail.com) and Morakinyo Ezekiel with email: (oluwanikhnyur@gmail.com)
