SixPi816
========

SixPi816 is a 65816 accelerator primarily targetting the Apple IIGS.

While a traditional accelerator works by interfacing a faster CPU to
the existing system, the core of SixPi816 is a software-emulated CPU
running on a Raspberry Pi.  A small amount of custom hardware allows
the Pi to be plugged ihe CPU socket of the target system as if it were
a normal 65816 CPU.

The main advantage of this design is simplicity. SixPi816 simulates
most system RAM on the Pi itself, meaning memory accesses can run at
full speed without needing complicated caching logic. Acceses to I/O
areas or to special memory (e.g. video RAM) will be passed through to
the host system as a regular bus access.

This project was inspired by the PiStorm project, which uses a similar
technique to provide a 68K accelerator for the Amiga line.
