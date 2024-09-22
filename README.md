# rom-sha1sum
This script calculates SHA-1 checksums for ROM files and ROM files inside ZIP archives, ignoring ROM headers. Which is particularly useful to check for romhack compatibility.

Currently only NES headers are ignored. Please let me know if there is demand for more headered file types.
The script requires GNU coreutils and at least Bash 4.4.

Sample output:

```
$ rom-sha1sum *.nes *.zip
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headerless).nes
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headered).nes [H]
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headered).nes [H] [zelda_headered.zip]
```
