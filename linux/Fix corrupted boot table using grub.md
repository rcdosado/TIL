Fix corrupted boot table
=======================

TIL how to restore partition chooser menu after its corrupted during installation of linux

*note* this requires that your partition is still not deleted and formatted

commands:

`sudo update -grub`

`sudo grub-mkconfig -o /boot/grub/grub.cfg`

the commands, lets you restore grub cfg after it auto detects partitions from the disk
