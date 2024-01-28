## UID: 605984742

## Pipe Up
The Pipe Up orgram simulates the behavior of the pipe operator in shell, allowing
users to execute multiple program in sequence using the output of one for the next

## Building
To build the program, I use the command make.

I broke the projects into pieces by working my way up from 0 to 2+ arguments. The program exits in error when no argument is provided. For one, it simply just calls execlp. For 2+, I used fork to create child processes and created fork to redirect 
input and output.

## Running
./pipe ls cat :
Makefile
pipe
pipe.c
pipe.o
\_\_pycache\_\_
README.md
test_lab1.py

./pipe ls cat wc : 
    7       7      63

./pipe : 
Error: Invalid argument

./pipe bogus
Error: execlp

## Cleaning up
Using make clean, I removed all compiled binaries generated during the build process