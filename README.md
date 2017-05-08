# RTL8723BS Wi-Fi
Realtek SDIO Wi-Fi driver

Tested on:
- Intel Compute Stick STCK1A8LFC

The BayTrail SDIO drivers require patches under the 4.9 Linux kernel.

### Patches
Verified against Linux kernel 4.9.13
Current dirver includes required patches:
- patches/
  - 0001-Add-pm_qos_cancel_request_lazy.patch
  - 0002-Disable-runtime-pm-when-sdio_irq-is-enabled.patch
  - 0003-Support-maximum-DMA-latency-request-via-PM_QOS.patch
  - 0004-Fix-device-hang-on-Intel-BayTrail.patch


### Firmware
Verified against Linux kernel 4.9.13
Current dirver includes required firmwares:
- firmware/
  - rtl8723bs_nic.bin


### Install
```
 make
 sudo make install
 sudo depmod -a
 sudo modprobe r8723bs
 
 ```
