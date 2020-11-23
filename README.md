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
`gnumeric`

:ledger: **Accounting system:**
`ledger`

:zap: **Torrent:**
`btfs`

:video_game: **Game development:**
`raylib`

:coffee: **Java:**
`gcc6-gcj`

:iphone: **Smartphone:**
`android-tools`

:pencil2: **Image editor:**
`gimp` `grafx2`

:black_nib: **Vector graphics editor:**
`inkscape`

:clapper: **Video editor:**
`handbrake`

:microscope: **Science:**
`octave` `R`

## To-do

- [ ] Finish `lxqt` DE
- [ ] Fix `openjdk-7-bootstrap` build
- [ ] Software i want to add
    - [ ] `0ad`
    - [ ] `iqmol`
    - [ ] `k2pdfopt`
    - [ ] `libreoffice`
    - [x] `octave` - with full features
    - [ ] `openshot`
    - [ ] `scribus`
    - [ ] `telegram-desktop`
    - [ ] `tg`
    - [ ] `vmd`

## KISS way

- [ ] Find a better repository structure.

- [ ] Completely remove `gettext` & `intltool` from packages which require them.
    - [x] `gimp`
    - [x] `gnumeric`
    - [x] `goffice`
    - [ ] `libmypaint`
    - [x] `lxmenu-data`
    - [ ] `pingus` - scons packages?

## Contributing

If you think something important is missing or should be different, open a pull request on this project.
If you have suggestions for improving this repository, open an issue on this project.
