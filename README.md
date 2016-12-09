# fix-chrome-aw-snap
on linux.

first watch /dev/shm how much mem that have. 
when this problem happen that because of low mem on /dev/shm
so resize it

open **nano /etc/fstab**

if is "**tmpfs      /dev/shm      tmpfs   defaults,size=64m   0   0**"

change it like "**tmpfs      /dev/shm      tmpfs   defaults,size=2g   0   0**"

if isn't then wrote this in end of file

**tmpfs      /dev/shm      tmpfs   defaults,size=2g   0   0**


then execute

$ **mount -o remount /dev/shm**


Ur Done.
