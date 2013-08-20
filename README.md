setupenv
========

This `bash` script provides a few functions that allow you to use an application installed into an arbitrary directory as if it were installed globally.  It does this by setting various environment variables that control which directories are searched for applications, manual pages, libraries, etc.

For example, if you install some GNU-style package with the usual commands

    ./configure --prefix=/my/favourite/directory
    make
    make install

and you `source` this script (e.g., in your `~/.bashrc` file)

    . /path/to/setupenv

then you can use the package after entering the following command:

    setupenv /my/favourite/directory

There's also a `removeenv` command to undo the changes, and `add_path` and `remove_path` to just add a single directory to the command line search `PATH` variable.
