# VirtualBot Driver
It is a serial port simulator for communication between Multi-agent Systems and a ChonBot virtualized.

## Installation
1) Install the dependencies. On your Debian-like Linux machine, run:

```console
user@machine:~$ echo "deb [trusted=yes] http://packages.chon.group/ chonos main" | sudo tee /etc/apt/sources.list.d/chonos.list
user@machine:~$ sudo apt update
user@machine:~$ sudo apt install linux-headers-`uname -r` chonos-virtualbot-driver
```

After the installation, by default, it will be instatiated on /dev many pairs of devices:

- /dev/ttyVB0 <---> /dev/ttyVBComm0
- /dev/ttyVB1 <---> /dev/ttyVBComm1
...

And so on. Writing on one device will make its content to be read on the other pair, and vice-versa

### Example:
In a terminal window, execute the command below to put the emulated port waiting for incoming data

```console
user@machine:~$ sudo javino listen /dev/ttyVBComm0
Hello Chon!
```
Open another terminal window and run the below command. On the first terminal Window. It should appear the 'Hello Chon!' message.

```console
user@machine:~$ sudo javino send /dev/ttyVB0 "Hello ChonBot!"
```
