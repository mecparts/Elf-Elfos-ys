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

Build 3 adds support for sending the file timestamp in block 0. Note
that Elf/OS has no concept of time zones and to be absolutely correct,
a time zone correction to the timestamp ought to be applied before
sending it. But it's good enough for now.

### Inspiration

* [Elfos-yr](https://github.com/dmadle/Elfos-yr)<br>
* [Elfos-Elf-xr](https://github.com/rileym65/Elf-Elfos-xr)<br>
