# ifspace

run a command if there is enough space in a filesystem


# To install

```sh
sudo make install
```


# To use

```sh
/usr/local/bin/ifspace [-h] [-v level] [-V] [-n] [-N] /filesys kbytefree cmd [arg ...]

    -h          print help message and exit
    -v level    set verbosity level (def level: 0)
    -V          print version string and exit

    -n          go thru the actions, but do not update any files (def: do the action)
    -N          do not process anything, just parse arguments (def: process something)

    /filesys    path of a file or direction on the storage device
    kbytefree   device holding /filesys must have at least kbytefree kilobytes tree to run cmd
    cmd         command to run if there is space
    [arg ...]   optional args to cmd

    NOTE: /filesys can be any path on the storage device: it does NOT need to be the mount point

Exit codes:
     0         all OK
     1         not enough space on /filesys
     2         -h and help string printed or -V and version string printed
     3         command line error
     4         /filesys path not found
     5         unable to determine the mount of free space on /filesys
     6         cmd exited non-zero
 >= 10         internal error

ifspace version: 1.3.1 2025-03-28
```


# Reporting Security Issues

To report a security issue, please visit "[Reporting Security Issues](https://github.com/lcn2/ifspace/security/policy)".
