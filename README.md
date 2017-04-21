# rtl8723bs
Realtek SDIO Wi-Fi driver

Tested on:
- Intel Compute Stick STCK1A8LFC

The BayTrail SDIO drivers require patches under the 4.9 Linux kernel.

Current dirver includes required patches:
- patches/ verified against Linux kernel 4.9.13


## Install

```
 make
 sudo make install
 sudo depmod -a
 sudo modprobe r8723bs
 
 ```
