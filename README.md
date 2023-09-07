# Creating all Sass folders and files with one command

## Introduction

While coding new web apps, one of the most boring parts is getting everything set up. While npm does most of the heavylifting for me (it creates all the Nextjs files), I still need to create all Sass files. Until now, I tried doing it manually, using the terminal to run each instruction individually, or even creating a repository with all the necessary folders and files. None of these really did it efficiently.

Now, the latest and most efficient solution I could think of is to add a shell command that does everything for me, and that's exactly what I've done. At the end of this tutorial, you'll be able to go to the project root folder, type `createsassfiles` (or something else you choose, but please keep reading), and everything will be set right for you.

## How to create the command

The first step is to download the [createsassfiles](./createsassfiles) file from this repository. I advise you to move it to a folder where you expect to store only custom shell commands. After that, you'll need to add this folder to your PATH, so open your terminal and type `pwd`. It'll give you the absolute path to your folder. Remember you can change the file name (don't rename it to an existing file, though) and the commands within it. You could, for instance, create different folders according to your needs. Moving on,

### Permanently

If you're using [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)), you have two options: to either modify the global shell configurations or just change your user's configuration file. To do that, you need to edit the file `/home/USER/.bashrc`. You can type `nano $HOME/.bashrc` to do so (`$HOME` is the same as `~/` or `/home/USER/`). Go to the end of the file and add the line `export PATH=$PATH:/$HOME/path/of/your/folder` **TWO IMPORTANT THINGS: remember that `$HOME` is the same as `~/` or `/home/USER/`, so make the changed to `path/to/your/folder` accordingly. More importantly,  you need the PATH=$PATH:/ at the beginning or you may remove all other folders from your PATH, making all other commands useless. If you mess things up, delete all new changes to `.bashrc` and type `source ~./bashrc` again.**. Save the modified file and type `source ~/.bashrc`. You can type `echo $PATH` to make sure everything worked. You can now use the command even after rebooting your PC.

### For this terminal window only

In order to create and use the custom command only for this terminal window, you should type `export PATH=$PATH:path/to/the/folder`. Again, this is only a temporary change and it won't work on other terminal sessions.


# Thank you for reading!

## Resources

[How to Add a Directory to PATH in Linux](https://linuxize.com/post/how-to-add-directory-to-path-in-linux/)

## Links

[My website](https://danieldevelops.tech/)
