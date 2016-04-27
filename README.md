# openwrt-go-patches

This a patches of gccgo and libgo for openwrt.

Copy 2 directories to openwrt buildroot directory.

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

If happen error:"crt1.o cann't found",create directory $(TOOLCHAIN_DIR)/gcc-5.3.0-final/i486-openwrt-linux-gnu/libs
,copy all files in $(TOOLCHAIN_DIR)/libgcc-dev/lib/ directoryto new created directory.
