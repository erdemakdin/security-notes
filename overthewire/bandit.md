## Level 0 > 1

Problem: The password was stored in a file called "readme" in the home directory

Solution: I list the files and the read it using 'ls' to list and 'cat' to read.

New commands: ls; lists files.
              cat; prints a files contents.  

Security angle: A password stored in a plain readable file can easily get accessed by anyone who want to see what inside of it.

## Level 1 > 2

Problem: The password was stored in a file called "-" in the home directory.

Solution: Since the files name is "-" the terminal reads it as it was a standard input, so it waits dor typing if you straight up wrote "cat -". For the solution, i chose to wrote "./" just before the "-". This prefixes the path so it reads the file named "-",rather than trying to do a commmand.

New solutions: "./"; these guys make it possible to read the file names that goes by hyphens.

Security angle: This might be a way to hide files, considering it makes finding the file a bit difficult.

## Level 2 > 3

Problem: The password was stored in a file called "--spaces in this filename--" in the home directory.

Solution: This time we still work with hyphens so we have to use "./" method, but also this time we have spaces inside of the filename. This makes the terminal reads every part of the file name that was seperated by the spaces searched seperatly. Since we have to get the terminal to make it read as a whole we write the filename inside of quotes. That way the terminal reads the filename as a whole.

New concepts: " "..." "; by using quotes around a file name that has spaces in it we make the name seem as a whole.

Security angle: Not requiring double quotes would make a script not read the intente file because of the spaces.

## Level 3 > 4

Problem: The password was stored in a file called "...Hiding-From-You" in the "inhere" directory.

Solution: Since it wasn't the home directory and it was "inhere" directory, i simply used "cd inhere" to change my directory. And then i used the "find" command that showed every file in that directory but there is the option to use "ls -a" which shows all file the same way. After i saw the file name was "/...Hiding-From-You" and it started with dots, i wrote "cat .//...Hiding-From-You" and accessed to the password.

Security angle: By using dots hackers can hide files. But with "find" or "ls -a" these hidden files comes out.