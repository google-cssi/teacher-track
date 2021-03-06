# Intro to Command Line

## Objective
***Students will be able to navigate their system’s file structure using the command line in
terminal.***

## SWABTS

+ CLI ‐ Understand and explain what terminal is and why we use it.
+ CLI ‐ Navigate through directories using relative and absolute paths*
+ CLI ‐ use the cd command to move up and down directories
+ CLI ‐ Use the ‘ls’ keyword to list items in a directory
+ CLI ‐ Remove a file and a directory by using ‘rm’ and ‘rm ‐rf’ keywords
+ CLI ‐ move files and directories using the mv command

## Motivation
Back in the day ('80s') computers only had a terminal to control them. (Show a picture). No mouse, no icons, no desktop. Just a blinking green cursor. You had to control your entire computer like that.

Later on, GUIs were created to make computers more accessible (like for your computer illiterate mom).
+ Developers continue to use the terminal instead of the GUI because it makes you faster, more in control, you understand what’s happening under the hood. If you’re a developer, time is money (and your time is expensive).
+ Understanding the terminal is like being Neo from the matrix- you can see the secret hidden files on your computer. (show cmatrix)
This is industry practice.

## Lesson Plan 

+ We’re going to learn about the command line by planning for a trip. Open your terminal and type `pwd`. (stop and have all students do this) `pwd` stands for print working directory. It will tell you where you are currently ‘standing’ in terms of directories. A directory is just a fancy shmancy word for a folder.

+ When you open your terminal you’ll see a tilde: `~`. This means you’re in your root. Logged in state of your computer

+ Let’s change directories. First check what directories are within the directory where you are standing by using `ls`, stands for list
+ then change directories using cd desktop command. cd into desktop. (stop and have all students do this) `cd desktop`

+ have students create a development directory `mkdir directory`

+ We’re going to make a new directory on the desktop for our trip. make a new directory called `trip` by using `mkdir trip`. Check and see that the directory was made by using ls. (stop and have all students do this)

+ Create directories for countries within the trip directory

+ Create directories for cities within the countries
(stop and have all students create countries and cities)

+ Create text files for places you want to visit in the cities directories by using touch. `touch city_name`

+ Use subl to open in sublime and add information about the eiffel tower, etc...

+ (pause and have students create files with text.)

+ remove a file that you no longer want using rm (I don’t want to see eiffel_tower.txt anymore) `rm eiffel_tower.txt`

+ remove an entire directory using rm -rf (remove paris directory) `rm -rf paris`

+ Accidentally place a file in the wrong directory so we need to move it. (washington_monument.txt in new_york directory needs to be moved to washington directory)

+ Practice moving up the tree using ..

+ Important: directories only know what’s directly inside of them. If I’m in Paris, the only things I know are the activities, I don’t know that I’m in France, and I don’t know that Rome even exists. 

+ Write out the relative path to the cities from the trip directory.

+ Write out the absolute path of different files and directories.


## Conclusion 
Command Line is an incredibly valuable tool that lets you maniplate configuration files of your computer. It also lets you navigate your computer much faster than using Finder. We will also use terminal to run our code, so familiarity with it is imperative.

## Hints and Hurdles
+ `~` is the logged in state for that particular user: ever log in to a home or school computer as a specific user? Just like that.
