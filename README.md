# 0x16. C - Simple Shell
## Compiled with gcc 4.8.4 using the flags -Wall -Werror -Wextra and -pedantic

## Overview

hsh Simple Shell emulates basic functionality of the UNIX Shell, a command line interpreter that reads commands from standard input and executes them.
Every hsh command follows the same general syntax: command name {arguments}.
That means that the command is executed by writing the name of the command followed by any arguments.
After receiving a command, our shell tokenizes it into words using " " as a delimiter.
The first word is considered the command and all remaining words are considered arguments to that command.

##Getting Started

First, clone this repository, then, compile this way: gcc  Wall  Werror -Wextra -pedantic *. c  o hsh
The Shell can work in interactive mode: $ ./hsh
                                        $ /bin/
                                        $ hsh main,c shell.c
or non-interactive mode: $ echo /bin/ls | ./hsh
                         $ $ hsh main,c shell.c

If there are no arguments and the standard input is connected to a terminal (Isatty), the shell is considered an interactive shell.
If the standard input is used with pipeline operator  |  to connect the command means the shell is in non-interactive mode.

##PATH

It is the separated list of directories in which the shell looks for commands.

##Builtins

There are some builtins programmed into hsh:

Env:
Prints the current environment.

Exit:
Terminates the shell process.