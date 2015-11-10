Dancepill
=========

Quick extract script for shell (currently only tested with Bash).

The problem
-----------

You want to extract a tarball or ZIP and you don't care what format it is to
pick up the right tool. The file does not need to have the correct extension.
And you want this fast, fallback method with Midnight Commander might be slow
due to zillion of IO terminal operations...

The Dancepill to the rescue!

    cd ~/bin
    git clone https://github.com/lzap/dancepill.git

And in your .bashrc do:

    source ~/bin/dancepill/dancepill

Logout or source it in your current terminal and start extracting:

    eeee tarball.tar.gz
    eeee tarball.tar.bzip2
    eeee tarball.xz
    eeee tarball.zip
    eeee whatever

There an function name called `dancepill` that does the extraction plus alias
`eeee` for it. Dancepill also installs `e` alias, but only in case it was not
yet used. If you still want to use this one, do this in your .bashrc:

    alias e=dancepill

Supported formats
-----------------

Format | Supported in
-------|-------------
7z     | 1.0
arj    | 1.0
bzip2  | 1.0
cpio   | 1.0
gzip   | 1.0
lha    | 1.0
rar    | 1.0
rpm    | 1.0
tar    | 1.0
xz     | 1.0
zip    | 1.0
iso    | 1.0

Additional features
-------------------

 * If the archive does not contain only one file or directory, dancepill will
   create an extra directory for you. No more extracted junk in the current
   directory!

 * If MIME is unknown, try to extract it with 7za or uncompress before giving
   an error.

License
-------

This is PUBLIC DOMAIN, do what you need to do. Pull requests appreciated!
