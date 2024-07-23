KDIR ?= /lib/modules/`uname -r`/build
MODULE_NAME = virtualbot

obj-m := $(MODULE_NAME).o

$(MODULE_NAME)-y := src/virtualbot_main.o

ccflags-y := -I$(src)/include

.PHONY: all all-dbg clean install uninstall modules_install

all: 
	$(MAKE) -C $(KDIR) M=$$PWD modules
	
all-dbg: 
	$(MAKE) -C $(KDIR) M=$$PWD EXTRA_CFLAGS="-DDEBUG" modules

clean:
	$(MAKE) -C $(KDIR) M=$$PWD clean
	
modules_install:
	sudo $(MAKE) -C $(KDIR) \
		M=$$PWD \
		modules_install 
	sudo depmod -A	

install:
	$(MAKE) -C $(KDIR) M=$$PWD modules_install
	depmod -A

uninstall:
	rm -f /lib/modules/$(shell uname -r)/kernel/drivers/$(MODULE_NAME)/$(MODULE_NAME).ko
	modprobe -r $(MODULE_NAME)
	depmod
	
tests:
	sudo dmesg -C
	sudo ./tests/tests_emulatedport_driver.py

