obj-m += seconds.o simple.o jiffies.o

all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

test:
	sudo dmesg -C
	sudo insmod simple.ko
	sudo rmmod simple.ko
	dmesg
