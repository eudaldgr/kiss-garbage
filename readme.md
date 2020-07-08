# :kiss: kiss-repo

:floppy_disk: A general purpose community repository

## Usage

```
$ # This repository needs official KISSLinux community enabled.
$ # Some packages like `lxqt` and `pingus` needs also the KISS-kde or kiss-games repositories.

$ git clone https://github.com/eudaldgr/kiss-repo
$ cd kiss-repo
$ for i in -- $(ls -d -- */); do export KISS_PATH=$PWD/$i:$KISS_PATH:; done

$ # Select a package to install
$ kiss b <pkg> && kiss i <pkg>
```

## Relevant end-user packages built

:page_with_curl: **Word processor:**
`abiword` `wordgrinder`

:bar_chart: **Spreadsheet:**
`gnumeric` `sc` `sc-im`

:ledger: **Accounting system:**
`ledger`

:earth_africa: **Web browser:**
`surf`

:zap: **Torrent:**
`btfs` `btpd`

:space_invader: **Games:**
`mgba` `pingus`

:coffee: **Java:**
`gcc6-gcj`

:iphone: **Chat:**
`tg` `birch`

:pencil2: **Image editor:**
`gimp` `grafx2`

:black_nib: **Vector graphics editor:**
`inkscape`

## Contributing

If you think something important is missing or should be different, open a pull request on this project.
If you have suggestions for improving this repository, open an issue on this project.
