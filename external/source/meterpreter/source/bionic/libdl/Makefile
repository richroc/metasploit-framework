CFLAGS= -nostdinc -nostdlib -fPIC -DPIC 
CFLAGS+= -I../libc/include -I../libc/private -I../libc/bionic -I../libc/kernel/arch-x86
CFLAGS+= -I../libc/kernel/common/linux/ -I../libc/arch-x86/include/ -I../libc/kernel/common/
CFLAGS+= -Os

CFLAGS+= -march=i386 -m32

all:
	gcc -Wl,--hash-style=sysv -shared -o libdl.so $(CFLAGS) libdl.c

debug: all

clean:
	rm libdl.so
