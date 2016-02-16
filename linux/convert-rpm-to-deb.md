# Convert RPM to DEB format in Ubuntu linux

To do this, we need an console application called alien .

Here are the steps:

1. fire up the terminal ctrl+alt+t
2. install alien utility, using the following command

```Bash

apt-get install alien

```

3. go to the location of your RPM file
4. type the following

```Bash

alien foo-1.1-2.rpm
ls -l

```

5. this will create foo-1.1-2.deb, you may now install it.


