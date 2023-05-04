
KDIR ?= /lib/modules/`uname -r`/build

MODULES_DEP = /lib/modules/$(shell uname -r)/modules.dep

# VirtualBot Driver name
VIRTUALBOT_NAME="virtualbot"

# VirtualBot device name
VIRTUALBOT_DEVICE=/dev/virtualbot

# Real Arduino device
# VIRTUALBOT_DEVICE=/dev/ttyACM0

.PHONY: all clean setup_dev_environment modules_install set_debug install modules_install tests

# setup-environment: configures environment for module development
# For Debian systems, start by using 'apt install make binutils'
# 1) It downloads the current system kernel headers 

all: 
	$(MAKE) -C $(KDIR) M=$$PWD modules

clean:
	$(MAKE) -C $(KDIR) M=$$PWD clean

modules_install:
	$(MAKE) -C $(KDIR) \
		M=$$PWD \
		modules_install 
	depmod -A

set_debug:
	dmesg -C
	sysctl -w kernel.printk=7
	sysctl kernel.printk
	
check_device_logs:
	dmesg

install:
	modprobe virtualbot
	chmod a+rw /dev/ttyVB0
	chmod a+rw /dev/ttyVBComm0

uninstall:
	rm -f /dev/virtualbot
	modprobe -r virtualbot
#	sudo rm -f /lib/modules/`uname -r`/extra/virtualbot.ko
	depmod

