# fast-forward

[![Build Status](https://travis-ci.org/phparsenal/fast-forward.svg?branch=master)](https://travis-ci.org/phparsenal/fast-forward) [![Dependency Status](https://www.versioneye.com/user/projects/558dbe19316338002400001c/badge.svg?style=flat)](https://www.versioneye.com/user/projects/558dbe19316338002400001c)

The PHP script will write the command you want to run in the batch file and afterwards it will be run.  
I could not find another way to `cd anotherdir` within PHP. chdir() didn't stick on the cli after the script exits. If you do know a way on Windows, please let us know how or send a pull request!


## Setup
Please run an initial `composer install` in the project folder to fetch the external libraries (a simple ORM and a CLI utility).

Afterwards make the `ff` command available globally:

### Windows
1. Edit the file `ff.bat` and change `ffpath` to the folder you put fast-forward in.
2. Copy `ff.bat` to a global path so that it is always available on the command line.

### Linux
1. Edit the file `ff.sh` and change `ffpath` to the folder you put fast-forward in.
2. Add this to your `~/.bashrc` or `~/.bash_aliases`  
    `alias ff='. /path/to/fast-forward/ff.sh'`

### Mac


## Usage
Add a new command in one line:  
`ff add <Shortcut> <Description> <Command>`

Do the same interactively:  
`ff add`

List all available commands and execute the selection:  
`ff`

Search for _htd*_  
If the only result is _htd_ it will be executed, otherwise all matches will be displayed first.  
`ff htd`
