# ys

## YMODEM send for Elf/OS

Usage:
```
   ys file1 [file2... filen]
```

"ys" is a YMODEM send program for Elf/OS. You can specify
multiple files on the command line, but not (yet?) wildcards.

### Status

Build 4 makes the code fast enough to catch the ACK and CRC/NAK at the
end of a block 0 send using the big banged UART. The price that had to
be paid was not being able to use the BIOS calls for the modem I/O
everywhere; it just wasn't quite fast enough.

It's currently set up to work on a Pico (Q & EF2, inverted). I do have 
some ideas about autodetecting what UART configuration is in use and 
patching the code on the fly, but it's just in my head at moment.

### Inspiration

* [Elfos-yr](https://github.com/dmadle/Elfos-yr)<br>
* [Elfos-Elf-xr](https://github.com/rileym65/Elf-Elfos-xr)<br>
