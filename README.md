# ys

## YMODEM send for Elf/OS

Usage:
```
   ys file1 [file2... filen]
```

"ys" is a YMODEM send program for Elf/OS. You can specify
multiple files on the command line, but not (yet?) wildcards.

### Status

Very, very alpha. It works; most of the time. The biggest hitch
at the moment is missing the ACK or CRC character after sending a
block, especially after the zero block containing the file name,
length and modification time. At the moment, I've added a couple of
stragetic 'sleep(1);' calls to lrz and that's got things ticking
along until I figure out how to make the 1802 code check things
quicker. 

And I haven't looked at converting the Elf/OS file timestamp to
a Unix "seconds since 1970 in octal" string yet. As I said, very,
very alpha.

### Inspiration

* [Elfos-yr](https://github.com/dmadle/Elfos-yr)<br>
* [Elfos-Elf-xr](https://github.com/rileym65/Elf-Elfos-xr)<br>
