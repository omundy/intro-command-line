# Command Line Intro

For humans to interact with a computer, we need an *interface*: a place where the human can somehow give the computer commands and the information it needs to carry out those commands.

What are some interfaces you know? What are some other possible interfaces?

## A Video Tour

Here's a video we made: <https://youtu.be/wowgqRyODCk>

It's worth watching even if you're already a little familiar with the command line. It's probably worth watching more than once. Try to follow along, don't just sit back and watch.

## The Command-Line

The command line is a non-graphical interface to your computer. All commands are issued by typing the name of a command and (typically) hitting enter/return.

A shell or command shell is a program that implements a command-line interface. Each shell might have slightly different conventions: what commands available, the names of those commands, how you refer to specific commands, how you give each command the information it needs to do its job.

But virtually every shell has the same 3-4 aspects:

1. You are presented with a "prompt" that often looks like `> ` or `$ ` or similar.
1. To run a command, you type the name of a command followed by a space-separated list of arguments and then hit enter.
1. The shell can only run one command at a time (there are some exceptions, but this varies widely between shells)
1. There is always a sense of "place" in the command line.
   With a GUI, you are always "outside" the desktop looking down from above. Your orientation with respect to the interface never changes.

   With a command line, it's more like you're a very tiny person living inside a specific folder/directory on your computer. There are special commands you can issue to move around, but there's always some *place* where you currently are.

   Most systems have a "default" place. In modern computers this is typically some kind of home directory.

   The your current location is called the **working directory**.

## Common Commands

Below are the most common commands. Commands have arguments. Required arguments are indicated by angle brackets `<likeThis>`. Optional arguments are indicated by square brackets `[likeThis]`.

When you type an argument, do **not** include the brackets. That syntax is a convention to indicate to you, the user, which argument are required vs. optional.

That is, if we say the command is `playSong <nameOfSong>` then the command would be

```console
playSong SomeCoolSong.mp3
```

It would **not** be

```console
playSong <SomeCoolSong.mp3>
```

In many shells, `<` and `>` have special meaning, so including them will produce surprising results.

### `pwd`

The `pwd` command stands for **p**rint **w**orking **d**irectory (some people say **p**resent **w**orking **d**directory). It prints out the current working directory.

### `ls [nameOfDirectory]`

**L**i**s**t the contents of the working directory. If `nameOfDirectory` is given, list the contents of that directory instead.

### `cd <nameOfDirectory>`

**C**hange the working **d**irectory to `nameOfDirectory`. For example, if the working directory contains a directory called `recipes` then this comand

```console
cd recipes
```

would change the working directory to `recipes`.

You can use `cd ..` to return to the previous directory you were in. For example, if you're in `/Users/jesse` and then run `cd Desktop`, your working directory will change to `/Users/jesse/Desktop`.

If you run `cd ..` you will return to `/Users/jesse`.

### `cp <originalFile> <newFile>`

Create a **c**o**p**y of `originalFile` named `newFile`.

### `mv <originalFile> <newFile>`

Move the file `originalFile` to `newFile`. If `newFile` is the name of an existing diretory, the file is moved into that directory. If no file exists with that name, effectively rename `originalFile` to `newFile`.

### `rm <file>`

**R**e**m**ove the file named `file`. Be careful, there's no undoing this!

### `mkdir <newDirectory>`

**M**a**k**e a new **dir**ectory named `newDirectory`. You'll get an error if a file or directory with the given name already exists.

### `touch <nameOfFile>`

If `nameOfFile` doesn't exist, creates an empty file with that name. Otherwise, updates the last-modified timetsamp of `nameOfFile`.

### `ps`

Display the **p**rocess **s**status, i.e., a list of the currently running processes (programs) on your computer. `ps` has many, many possible arguments.

By default it only lists the processes running in the current shell. If you want to see all the processes on the entire computer, run

```console
ps aux
```
