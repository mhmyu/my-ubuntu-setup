> notes
# clean snap packages
- create new file `clean-snap.sh`
    ```
#!/bin/bash
# Removes old revisions of snaps
# CLOSE ALL SNAPS BEFORE RUNNING THIS
set -eu
snap list --all | awk '/disabled/{print $1, $3}' |
    while read snapname revision; do
        snap remove "$snapname" --revision="$revision"
    done
    ```
- run `sudo bash clean-snap.sh`

# apps
- [Bottles](https://usebottles.com/) `easily run Windows software on Linux with Bottles!`
- [ksnip](https://github.com/ksnip/ksnip) `ksnip the cross-platform screenshot and annotation tool`
- [sleek](https://github.com/ransome1/sleek) `todo.txt manager for Linux, Windows and MacOS, free and open-source (FOSS)`
