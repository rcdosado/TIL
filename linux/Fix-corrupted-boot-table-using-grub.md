Fix corrupted boot table
=======================

TIL how to restore partition menu after its corrupted during installation of linux
basically it just scans partitions and detects if its bootable if not. 

*note* this requires that your partition is still not deleted and formatted

commands:

`sudo update -grub`

`sudo grub-mkconfig -o /boot/grub/grub.cfg`


