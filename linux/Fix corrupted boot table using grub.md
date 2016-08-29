Fix corrupted boot table
=======================

TIL how to restore partition chooser menu after its corrupted during installation of linux

*note* this requires that your partition is still not deleted and formatted

1. first command

`sudo update -grub`

2. second command
`sudo grub-mkconfig -o /boot/grub/grub.cfg
