Small overview of the very basic unix **binaries** and **shell builtins**, every user should know. This document assumes that you know how a computer operating system works.

## Get help with "`COMMAND`"

- Check out a commands' reference using the `COMMAND --help` flag
- Use the `type COMMAND` builtin to find out if it's a real program (a binary) or captured by the shell in advance (a shell builtin)
- Most programs are traditionally documented with `man COMMAND` (manual) pages

I strongly recommend installing [tldr](https://github.com/tldr-pages/tldr#readme) (Too long; didn't read). Use `tldr COMMAND` to find out what any given command does. It lists some simple and modern day, usage examples. Remember to RTFM, and happy hacking.

## Basics

You can _enter_ the path of any [computer program](https://en.wikipedia.org/wiki/Computer_program) to run (execute) it. For example: `./start-server`, `/bin/ls` or `/bin/bash`. Below are some very basic programs (binaries) available on **any unix system** by default (guarenteed to be in `$PATH`). Remember to use the `cd DIRECTORY` shell builtin to navigate the PWD.

```sh
# List files in a directory
ls DIRECTORY
# Read bytes of a file
cat FILE

# Create an empty file
touch FILE
# Make a new directory
mkdir DIRECTORY

# Remove a file
rm FILE
# Remove a directory recursively
rm -r DIRECTORY
```

## Scripting

You can assign expressions as strings to a variable using `=` and retrive them with `$`. i.e. `ip=1.2.3.4; echo $ip`. Use quotes to escape spaces on the prompt, you can quote anything, i.e. `'ls'`.

```sh
# Set a shell variable
VARIABLE=VALUE

# Set an environment variable
export VARIABLE=VALUE

# Run a `.sh` shell script (in the current shell)
source FILE

# Find out how the shell would resolve
type COMMAND
```
