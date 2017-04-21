# rtl8723bs
Realtek SDIO Wi-Fi driver

Tested on:
- Intel Compute Stick STCK1A8LFC

Do verify that the device is listed under ```/sys/bus/sdio/```

Note that on all those tablets, you will need to apply a few patches because
to the BayTrail SDIO drivers:
http://thread.gmane.org/gmane.linux.kernel.mmc/25081/focus=25087
http://thread.gmane.org/gmane.linux.kernel.mmc/31583
For older kernel than 4.3, you might also need this patch applied:
https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=d31911b9374a76560d2c8ea4aa6ce5781621e81d

You can find these patches in the following directories:
- `patches/` for Kernel 4.9.13

## Install

```
 make
 sudo make install
 sudo depmod -a
 sudo modprobe r8723bs
 
 ```
