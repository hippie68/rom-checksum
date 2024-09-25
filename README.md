# rom-checksum
This script calculates both file checksums and (if supported) ROM checksums for ROM files and ROM files inside archives. Which is particularly useful to check for romhack compatibility.

The script requires GNU coreutils and at least Bash 4.4. It runs on Linux, WSL, Cygwin, Git for Windows, and other compatible platforms.  
For archive support, the following programs are required:
- unzip for .zip files
- gunzip for .gz files
- 7za for .7z files
For optional CRC32 support, the Perl script "crc32" is required, which for Debian-based distros is included in the package "libarchive-zip-perl".

Usage:
```
Usage: rom-checksum FILE/DIRECTORY [...]

Options:
  -e LIST  Only process files whose file extensions are specified in comma-
           separated argument LIST (without dots).
  -r       Parse directories recursively.

```

Sample output:

```
$ rom-checksum zelda.zip
The Legend of Zelda.nes < zelda.zip
File CRC32: 316CFF69
File MD5: 4156F66C0FAC36222B5A1DA05DB85D68
File SHA-1: 799459548F9636DD263200DA494F04058F5540E2
ROM CRC32: 3FE272FB
ROM MD5: D9A1631D5C32D35594B9484862A26CBA
ROM SHA-1: A12D74C73A0481599A5D832361D168F4737BBCF6
```

The script displays file checksums for all files, but ROM checksums are currently only supported for NES ROMs. Please let me know if there is demand for more headered file types or if a ROM file extension is missing.
