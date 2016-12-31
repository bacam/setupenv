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

Other commands:

* `removeenv` undos the changes from `setupenv` for the given path
* `printsetup` lists all of the directories that you have set up
* `add_path` adds a single directory to the command line search `PATH` variable (and nothing else)
* `remove_path` undos an `add_path`
* `printpath` prints `PATH` in a more readable form
