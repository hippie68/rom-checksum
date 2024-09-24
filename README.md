# rom-sha1sum
This script calculates SHA-1 checksums for ROM files and ROM files inside archives, ignoring ROM headers. Which is particularly useful to check for romhack compatibility.

The script requires GNU coreutils and at least Bash 4.4. It runs on Linux, WSL, Cygwin, Git for Windows, and other compatible platforms.  
For archive support, the following programs are required:
- unzip for .zip files
- gunzip for .gz files
- 7za for .7z files

Sample output:

```
$ rom-sha1sum *
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headerless).nes
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headered).nes [-H]
799459548f9636dd263200da494f04058f5540e2  The Legend of Zelda (headered).nes [+H]
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headered).nes [-H] < zelda_headered.zip
799459548f9636dd263200da494f04058f5540e2  The Legend of Zelda (headered).nes [+H] < zelda_headered.zip
```

Instead of:

```
$ sha1sum *
a12d74c73a0481599a5d832361d168f4737bbcf6  The Legend of Zelda (headerless).nes
799459548f9636dd263200da494f04058f5540e2  The Legend of Zelda (headered).nes
7dc9ee45e1ba0395e69e99a2bc36649e0a8e03fc  zelda_headered.zip
```

Currently only NES headers are ignored. Please let me know if there is demand for more headered file types.
