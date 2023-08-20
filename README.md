 # MrMessy
Jack Audio X11 apps for audio visualization
===========================================

The apps show themselves as a kind of 'virtual instruments' on your desktop.

Funfacts:
1) The pictures of the instruments are from ones that I own personally.
2) All controls can have callable code, currently only the powerbuttons work
3) The instruments are resizeable in the most strangest of ways.
4) Press the top-left corner of an instrument, to have the window as a borderless desktop app

Current state: Initial commit
Source is still a bit messy, lots of viral introns in code

Platforms:
----------
linux with X11, Xext, and Jack dev libraries.

e.g. ubuntu:
apt install x11proto-dev libjack-dev

How to Compile (currently):
---------------------------

./make.sh

How to run
----------

spectrum analyzer:
(bash)$ ./xdisp

![spectrum-analyzer](https://github.com/noudio/MrMessy/blob/main/doc/xdisp-spectrum-analyzer.png)

scope:
(bash)$ ./xdisp --scope

![scope](https://github.com/noudio/MrMessy/blob/main/doc/xdisp-scope.png)

scope:
(bash)$ ./xdisp --black

![scope](https://github.com/noudio/MrMessy/blob/main/doc/xdisp-black.png)

This one can be useful for video grabbing, due to the black background. I used it for example to create this youtube vid:
[andjelisa on rararadio](https://youtu.be/DI8FW4kV9h8?list=PL6jUM7gk5v0XpZLoLPm6GyWbw1ySJ1M1x&t=6864)


By default 'xdisp' only creates jack ports, but it doesnt connect them.
Use jackctl patch bay to setup automatic connections.
Or otherwise ./xdisp [--connect] makes an automatic connection to the writers of the
system output