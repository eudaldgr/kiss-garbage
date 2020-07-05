# kiss-repo

A compilation of all my repositories

## Usage

```
$ git clone https://github.com/eudaldgr/kiss-repo
$ cd kiss-repo
$ for i in $(ls -d */); do export KISS_PATH=$PWD/$i:$KISS_PATH:; done

$ # Select a package to install
$ kiss b <pkg> && kiss i <pkg>
```
