### IF.03.01 Procedural Programming

## Objective
The goal of this assignment is to make you familiar with a first C program and the tool chain how to build it.

## Materials

- Visual Studio Code
- gcc
- terminal.

## Required Tasks
1. We will do all our examples under Linux / Unix. So if you are running your machine under Linux oder macOS you are already done and may go to the next section.
If you run your computer under Windows, you have to do a bit of preparation work. First of all you have to install [Windows Subsystem for Linux (WSL2)](https://docs.microsoft.com/en-us/windows/wsl/install-win10). Instructions can be found by following the previous link. In a second step you have to install  [Docker Desktop for Windows Home](https://docs.docker.com/docker-for-windows/install-windows-home/) if you have Windows Home. In case you have Windows Pro, Enterprise or Education you have to install [Docker Desktop for Windows](https://docs.docker.com/docker-for-windows/install/).

1. Install `git` on your computer as explained on the [Git installation page](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

2. Set up a directory `PRPR` in the directory `Documents` of your home directory (in the Terminal or PowerShell) and change into this directory.

2. Accept the Github Classroom assignment and clone the repository
   1. Green Button "Code"
   2. Copy the URL on top of the drop down menu
   3. Change to your Terminal/PowerShell and type `git clone <paste copied url>`
   4. Figure out the name of the newly created directory by typing `ls -l` and change into this directory

3. Start Visual Studio Code either via the Gui or by typing `code .` into your Terminal or PowerShell. Type the program `hello_world.c` with Visual Studio Code as given in the lecture’s template. Don’t forget the block header comment on top of the file and adjust it according to your personal data (your name should be really your name, etc.). The [block header comment](https://github.com/if-03-22-prpr/if.03.22-01_hello-world/blob/master/sample_block_header.txt) is also part of the starter code of your repository. Now you are ready to try out your program.

3. (Only for Windows users) Under Windows you have to start your Docker environment. For this you open a cmd Window and change to the directory with your program `cd Documents\PRPR\01_hello_world`. Then you start a Docker image prepared for you by `docker run -it -v "%CD%":/new bauepete/prprubuntu:firsttry`. Now you should have an Ubuntu image running on your machine. By `cd /new` and `ls -l` you should see the content of your current working directory under Windows.

4. Now everybody should be ready to compile and link the program: `gcc -o hello -Wall -pedantic -std=c99 hello_world.c`. If this runs without any errors (i.e., no feedback from the Terminal) an executable should have been created from your source file. Type `ls -l` and watch out for a file called `hello`. You can start the program by typing `./hello`.

4. Commit your changes by typing
   1. `git add .` (Selects the newly created file to be added to the tracking list of your repo)
   2. `git commit -m "Hello world compiles and runs"` (Commits your changes to the repository

4. **IMPORTANT:** Change the program such that it does not print ”Hello, World” but your complete name (i.e., first name and last name) instead of ”World”. For example in my case the program should print out ”Hello, Peter Bauer”. Change the source code accordingly, recompile and test the program.

5. Commit your changes by typing
   1. `git add .` (Selects the changed file to be added to the tracking list)
   2. `git commit -m "Prints my name instead of world"`

5. Finally make a screen shot of this terminal window, name it `hello_me.png` and add it to your working directory. Take care that the screenshot is in a shape that one can read the content of the terminal. See a sample screenshot below:

![a sample screen shot](screenshot.png)

6. Commit your changes and push your solution to the central repo by typing
   1. `git add .` (adds all changed and newly created files to the tracking list of your repo)
   2. `git commit -m "Final solution"` (Commits your changes)
   3. `git push` (Pushes all changes to the central repo and makes it visible for grading)

## Evaluation
All coding assignments will get checked. Most common reasons that your assignment is marked down are:

- Program does not build or builds with warnings
- One or more items in the *Required Tasks* section are not satisfied
- Submitted code is visually sloppy and hard to read

## Things to Learn
- Output in C
- Build C Programs
- Run programs from the terminal
- Work with the terminal

