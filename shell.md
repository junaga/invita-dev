Small overview of the very basic unix **binaries** and **shell builtins**, you _should_ know about. This document assumes that you know, how a computer operating system works. Remember to RTFM, and happy hacking.

## Basics

You can _enter_ the path (location), of any [computer program](https://en.wikipedia.org/wiki/Computer_program) (binary) to run (execute) it. For example: `./init-server` or `/bin/lsblk`. Below are some very basic programs available by default, guarenteed to be in `$PATH`, on _any_ unix system.

Use the `cd DIRECTORY` shell builtin to navigate. _(change the process environment working directory)_

```sh
# Read bytes of a file
cat FILE
# List files in a directory
ls DIRECTORY

# Create a new empty file
touch FILE
# Write any output to a new or existing file
cat FILE.old >> FILE.new
# Edit a new or existing file
# `$EDITOR` should be `nano`, `vim`, `emacs`, `code`.. etc
$EDITOR FILE
# Make a new directory
mkdir DIRECTORY

# Remove a file
rm FILE
# Remove a directory (recursively)
rm -r DIRECTORY
```

## Get help with "`COMMAND`"

I strongly recommend installing [tldr](https://github.com/tldr-pages/tldr#readme) (Too long; didn't read), to find out what any given command does. It lists some simple and modern day, usage examples.

```sh
# If you installed tldr
tldr COMMAND

# Programs usually carry a reference about themselfs
COMMAND --help
# Programs have versions.
COMMAND --version

# Things are traditionally documented in manual pages
man COMMAND
```

Of course there is always https://www.google.com/search?q=linux+COMMAND

## Scripting

You can assign expressions as strings to a variable using `=` and retrive them with `$`. i.e. `ip=1.2.3.4; echo $ip`. Use quotes to escape spaces on the prompt, you can quote anything, i.e. `'ls'`.

```sh
# Is it a real program (a binary) or captured by the shell (a shell builtin)
type COMMAND

# Set a shell variable
VARIABLE=VALUE
# Set an environment variable
export VARIABLE=VALUE
# Get any variable
$VARIABLE

# In the current shell, run a `.sh` shell script
source FILE
```
