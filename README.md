# openwrt-go-patches

Copy directories to openwrt buildroot directory.

make menuconfig


	Advanced configuration options (for developers)  --->
	    Toolchain Options  --->
	        [x] Build/install gccgo compiler
	        --- C library implementation --->
		            [x] Use glibc

make -j1 V=s



If "error: crt1.o can't found"
	
	mkdir -p $(TOOLCHAIN_DIR)/gcc-5.3.0-final/lib/gcc/i486-openwrt-linux-gnu/5.3.0/
    mkdir $(TOOLCHAIN_DIR)/gcc-5.3.0-final/i486-openwrt-linux-gnu/libs
    cp -r $(TOOLCHAIN_DIR)/libgcc-dev/lib/ $(TOOLCHAIN_DIR)/gcc-5.3.0-final/i486-openwrt-linux-gnu/libs
