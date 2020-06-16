CC_PATH=/home/hyq/ws/h5/aw_h5_2mic/lichee/tools/build/toolchain/gcc-linaro-arm-linux-gnueabihf-4.9-2014.08_linux/bin
CC = $(CC_PATH)/arm-linux-gnueabihf-gcc
LD = $(CC_PATH)/arm-linux-gnueabihf-ld
OBJCOPY = $(CC_PATH)/arm-linux-gnueabihf-objcopy

all : start.o
	$(LD) -Taboot.lds -o gboot.elf $^
	$(OBJCOPY) -O binary gboot.elf gboot.bin

%.o : %.S
	$(CC) -g -c $^
%.o : %.c
	$(CC) -g -c $^


clean:
	rm -rf gboot.elf gboot.bin *.o
