# Change Username in Ubuntu

changing username is not easy to do given the number of steps it needs.
condensed from a webpage here http://askubuntu.com/questions/558669/renaming-user-name

Here are the steps:

-1. you need to add another Admin account for this to happen
0. login using that account(not the one you would change)
1. fire up the terminal ctrl+alt+t
2. you cannot change your own username, because it needs killing your own process
so you will have to login as another admin user, and apply commands for that

    ```Bash

   	sudo -i
	killall -u oldname
	id oldname
	usermod -l newname oldname
	groupmod -n newname oldname
	usermod -d /home/newname -m newname
	usermod -c "New_real_name" newname
	id newname
    ```

3. restart.

