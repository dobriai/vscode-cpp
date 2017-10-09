# Visual Studio Code with C/C++

This is just a small repo for testing VSCode setup for using with C/C++ on various platforms.

The original and very good instructions on how to do it all are here: https://code.visualstudio.com/docs/languages/cpp

# Using with `gcc` on a Linux macine

## Setup
Not much to do. Just check that you have `gcc` (a.k.a. `g++` when compiling C++ code) and `gdb`. Most distros do have these, but it does not hurt to check:
```
which g++
which gdb
```
should yield something like this:
```
~ > which g++
/usr/bin/g++
~ > which gdb
/usr/bin/gdb
```

Clone the repo. Make sure you check out the correct branch, if the default one is not what you want.

In a terminal, `cd` to the repo that you cloned and start `code` from there, e.g.:
```
~ > cd ~/tmp/vscode-cpp
~/tmp/vscode-cpp(linux-gcc) $ code .
```

## Building, running, debugging
If all goes well, `ctrl-shift-B` should make it build. Or, run it from the _Tasks_ menu. Or search the build command globally - `ctrl-shift-P`.

Then `F5` will start a run. One can set breakpoints and inspect variables.
