# The Command Line

The terminal is an interface with the operating system at its most simple level. Text

# Unix Philosophy

<blockquote>
"Write programs that do one thing and do it well. Write programs to work together. Write programs to handle text streams, because that is a universal interface." - Doug McIlroy
		Most of the fist functions you will learn and use on a regular basis will only have one small job.
</blockquote>

# The Basics

## Getting help

### Read the manual

man (manual)

Options/flags
 flags are options that can be run with a command.
To find out a commands flag one can generally type a command using the flag --help.
Flags start with - or -- and 
(generally 
example: man man
	Movement
	cd (change directory)
symbols
~ home
/ root
. Current directory
.. Parent directory

Defaults to home
# CRUDing

__C__reate
__R__ead
__U__pdate
__D__delete

(but not in that order)
(Today we will be stating with basic file manipulation)
(a common techie concept is CRUD)
(But we will be starting with Reading)

## cRud

# Reading the file system

## ls - list

Defaults to current directory

### sample output

aptdaemon-wVVqMP  hsperfdata_root  sni-qt_skype_7507-pMW0rV  ycm_temp
cvcd              orbit-josh       ssh-KbkbT3y7MaZA          qtsingleapp-homejo-b07c-3e8
foo               plugtmp          tmux-1000                 qtsingleapp-homejo-b07c-3e8-lockfile
hsperfdata_josh   skype-7507       v31tyhs                   tmp66LAAe


(Lets see what we can do with the flags.)
(Running help is going to provide a lot of options that we don't have time to cover here so we will only look at the two most commonly uses ones.)

# -l
Use a long listing format

@@@
ls -l                                                                                                       ⏎
total 56
drwx------ 2 josh josh 4096 Sep 11 09:56 aptdaemon-wVVqMP
drwx------ 2 root root 4096 Sep  9 09:07 cvcd
drwxrwxr-x 3 josh josh 4096 Sep 10 16:21 foo
drwxr-xr-x 2 josh josh 4096 Sep 11 09:55 hsperfdata_josh
drwxr-xr-x 2 root root 4096 Sep 11 09:58 hsperfdata_root
drwx------ 2 josh josh 4096 Dec 31  1969 orbit-josh
drwx------ 2 josh josh 4096 Sep 11 09:44 plugtmp
@@@

# -a, --all

Do not ignore entries starting with .

@@@
.                          cvcd             orbit-josh                tmux-1000   qtsingleapp-homejo-b07c-3e8
..                         foo              plugtmp                   v31tyhs     qtsingleapp-homejo-b07c-3e8-lockfile
aptdaemon-wVVqMP           hsperfdata_josh  skype-7507                .wine-1000  tmp66LAAe
.com.google.Chrome.9pVhQ1  hsperfdata_root  sni-qt_skype_7507-pMW0rV  .X11-unix   .X0-lock
@@@

## What does a dot have to do with anything?

Dot files are hidden files on a Unix file system.

* generally settings files
* or application data
* Works like the Windows registry.

# Reading files
___more___ or ___less___

## Crud

# Creating Things

## Folders

mkdir foo

Wait theres more that you can do with that command. What if you wanted to create a child directory of, foo?

@@@
~/D/s/comandlinebasics git:master ❯❯❯ mkdir --help        
Usage: mkdir [OPTION]... DIRECTORY...
Create the DIRECTORY(ies), if they do not already exist.

Mandatory arguments to long options are mandatory for short options too.
  -m, --mode=MODE   set file mode (as in chmod), not a=rwx - umask
  -p, --parents     no error if existing, make parent directories as needed
  -v, --verbose     print a message for each created directory
  -Z, --context=CTX  set the SELinux security context of each created
                      directory to CTX
      --help     display this help and exit
      --version  output version information and exit
@@@

### What Flag would allow me to create the directory and sub directories

foo/bar/public_html, in a single command?

    
    Creating files
    touch

## Files
  
  touch

(touch can be used for more than just creating a file. It can also be used to update certain meta data of a file, suchh as last updated date.  I have never used any of the flags in touch)

## crUd

# Editing/updating

mv = move

(used for moving files and folders another location.
Commonly used for renaming a folder)

## Updating files

Vim and Nano

    Using Vim (basics)

(Stands for vi improved)

Vi was made before the mouse was invented.

(the developers realized that they needed a more efficient way of running commands and moving around than menus and arrow keys. so there are 3 primary modes of operation in Vim

### Normal mode

http://www.viemu.com/vi-vim-cheat-sheet.gif


### Insert modes

### Visual mode

(the most of the movement and edit functions will work well but I want to mention Y for yank and D for delete, but it will also serve as a Cut function. You can P to paste the deleted or yanked string.)

### common commands

:w write file
:q quit
:help
commands may be combined
save and quite :wq

    Nano Basics

    image

## cruD

# Deleting Things

rm

all you need to delete everything.
This is the really real world, their aint no coming back.
(there is no recycling bin here recovering files can be extremely difficult)

(again the the --help flag output is to long for a slide but we will cover the ones I use the most)

### -f, --force

 rm -f file
 (forces the deletion of the file. With out it it will give you an are you sure prompt)

### -d, --dir

rm -d directory

(deletes an __empty__ directory)
(to delete a populated directory you will need to combine the two above flags.)

# Shell flavors

A shell is the interface that is presented to the user of the command line.
They provide goodies like 

* history
* auto completion
* custom settings

By default almost every one will be using a shell called BASH.

(BASH version one was released in 1989, version 4.7 was pleased this past Feb)

(In the last few years a newer shell has been becoming more popular called Zshel)
(Zshel take all of peoples fav things of about bash and improves on it)

    Using system variables and intro to the bash profile
    Powering up your terminal: Using Zshel
    Prettyfing your terminal with themes and colors
    Any other stuff to do with a terminal
