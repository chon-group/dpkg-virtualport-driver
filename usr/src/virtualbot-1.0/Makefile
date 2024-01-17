KDIR ?= /lib/modules/`uname -r`/build
MODULE_NAME = virtualbot

obj-m := $(MODULE_NAME).o

$(MODULE_NAME)-y := src/virtualbot_main.o

ccflags-y := -I$(src)/include -DDEBUG

.PHONY: all clean install uninstall

all: 
	$(MAKE) -C $(KDIR) M=$$PWD modules

clean:
	$(MAKE) -C $(KDIR) M=$$PWD clean

install:
	$(MAKE) -C $(KDIR) M=$$PWD modules_install
	depmod -A

uninstall:
	rm -f /lib/modules/$(shell uname -r)/kernel/drivers/$(MODULE_NAME)/$(MODULE_NAME).ko
	modprobe -r $(MODULE_NAME)
	depmod