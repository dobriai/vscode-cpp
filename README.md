# Visual Studio Code with C/C++ 

This is just a small repo for testing VSCode setup for using with C/C++ on various platforms.

The original and very good instructions on how to do it all are here: https://code.visualstudio.com/docs/languages/cpp

# Using with CYGWIN

## Setup
Make sure you have `cygwin` installed and you have the `g++` and `gdb` packages. Those may not be installed by default, so check it out:
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

Open a **`CYGWIN` terminal**, i.e. not a `Git` one or a Windows terminal!

`cd` to the repo that you cloned and start `code` from there, e.g.:
```
~ > cd /e/GitHub/vscode-cpp
/e/GitHub/vscode-cpp >code .
```

By starting from a `cygwin` terminal, you set-up `code` with all the cygwin-ish environment vars, so it can find `g++`, `gdb.exe` and all sorts of DLLs without specifying full paths. This should hopefully save some trouble!

### In case some .exe cannot be found and full Windows paths are needed

If something cannot be found, here is how one can discover the full windows path of an executable, e.g. `gdb`:
```
cygpath.exe -aw `which gdb`
```
If this needs to be added to any config file, one will likely have to add the `.exe` extension and escape the \\-s to end up with something like this:
`"C:\\cygwin64\\bin\\gdb.exe"` (on my machine I have `cygwin` installed in _c:\cygwin64_).

## Building, running, debugging
If all goes well, `ctrl-shift-B` should make it build. Or, run it from the _Tasks_ menu. Or search the build command globally - `ctrl-shift-P`.

Then `F5` will start a run. One can set breakpoints and inspect variables.
