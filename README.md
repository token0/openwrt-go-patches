# openwrt-go-patches

This a patches of gccgo and libgo for openwrt.

Copy three directories to openwrt buildroot directory.

git clone https://github.com/GeertJohan/openwrt-go

git checkout add-gccgo-and-libgo

make menuconfig

-> Advanced configuration options

-> Toolchain options

....
-> Select Build/Install gccgo

....

-> C library implementation

-> Use eglibc

make V=s

If happen error:"crt1.o cann't found",create directory $(TOOLCHAIN_DIR)/i486-openwrt-linux-gnu/lib,copy all files in $(TOOLCHAIN_DIR)/libgcc-dev/lib/ directory
to new created directory.
