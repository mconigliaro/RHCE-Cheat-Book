# Understand and use essential tools

## Access a shell prompt and issue commands with correct syntax

To access a shell prompt: `Ctrl`+`Alt`+`F2`

## Use input-output redirection (>, >>, |, 2>, etc.)

### Input redirection from files

Execute `command` using `file` as the source of input:

`<command> < <file>`

### Output redirection to files

Execute `command` and redirect **STDOUT** to `file`:

`<command> > <file>`

Execute `command` and redirect **STDERR** to `file`:

`<command> 2> <file>`

Execute `command` and redirect both **STDOUT** and **STDERR** to `file`:

`<command> &> <file>`

Note that `>>` can be used in place of `>` to append to the destination file instead of overwriting it.

### Piping

Execute `command1` and redirect **STDOUT** to `command2`:

`<command1> | <command2>`

Execute `command1` and redirect both **STDOUT** and **STDERR** to `command2`:

`<command1> 2>&1 | <command2>`

## Use grep and regular expressions to analyze text

`grep [options] <regexp> <file>`

## Access remote systems using ssh

`ssh [options] [user@]<host>[:port]`

## Log in and switch users in multiuser targets

`su - <user>`

## Archive, compress, unpack, and uncompress files using tar, star, gzip, and bzip2

## Create and edit text files

## Create, delete, copy, and move files and directories

## Create hard and soft links

## List, set, and change standard ugo/rwx permissions

## Locate, read, and use system documentation including man, info, and files in /usr/share/doc
