To run the code, use the given makefile, which generates main as output file.

Files and their uses:<br>
    Headers:<br>
        1.header.h contains all the system header files to be included<br>
    C files:<br>
        1.execvp.c contains the functions for foreground and background process. <br>
        2.echo.c includes the echo function.<br>
        3.cd.c contains the functions for changing directory.<br>
        4.main.c is the main program.<br>
        5.exit.c exits the shell.<br>
        6.history.c includes history of previous commands.<br>
        7.ls.c includes ls functions.<br>
        8.nightswatch.c includes the nightswacth function.<br>
        9.pinfo.c includes pinfo function.<br>
        10. pwd.c includes pwd function.<br>

The Shell program runs on an infinite loop and takes input from stdin using fgets(), which is further tokenized into semicolon-separated commands, which are run in order. Each command is tokenized separating the commands,flags(if any) and the arguments(if any). Switch-case is used in order to select from the executable commands like rm,mkdir etc and other self-defined commands pwd, ls, cd, echo, pinfo,nightswatch and history.

Assumptions made:
    1. /proc filesystem is accessible as is to any standard linux user.<br>
    2. no of semicolon separated commands is maximum 50, with 2000 char as max length for each.<br>
    3. each command can have maximum value of x as 50, where argv[x].<br>
    4. username, hostname and cwd are 1000 characters at max.<br>

Only bonus implemented is history command
