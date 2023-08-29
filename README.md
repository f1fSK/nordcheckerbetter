# nordvpn-checker

A simple Python script to check if NordVPN accounts listed in a file are valid.

### NOTE: This script only works in Linux.

# Requirements

- The NordVPN CLI tool. [Get it from here](https://nordvpn.com/download/linux/).
- [Python 3.7](https://www.python.org/downloads/).
- An input file containing NordVPN login entries in `email:password` format.

# Installation

- Clone the repo with `git clone https://github.com/behnambm/nordvpn-checker`

# Code format
The Uncompromising Code Formatter [Black](https://github.com/psf/black5)

```
$ black -t py38 nord-checker.py
```

# Usage

- The syntax is
  > `nord-checker.py [--file | -f] path/to/file [--output | -o] path/to/file [--connect | -c] [--delete | -d]`

- Arguments
```
  -f FILE, --file FILE  The file that contains your email:password entries
  -o FILE, --output FILE
                        The file to output the successful email:password entries to
  -c, --connect         login & connect
  -d, --delete          remove faulty password lines in input-file
```
For example, `cd` into the recently cloned directory and run:

```
$ python nord-checker.py --file accounts.txt --output success.txt
```

If you just want to connect you can use: 
(The first successful connection will exit this script)

```
$ python nord-checker.py --file succes.txt --output /dev/null -c
```


