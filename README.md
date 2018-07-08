# RTL8723BS Wi-Fi
Realtek SDIO Wi-Fi driver

Tested on:
- Intel Compute Stick STCK1A8LFC
- Alfawise X5 (Debian 9 kernel 4.9)

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
  - rtl8723bs_ap_wowlan.bin		*[Unused in current configuration]*
  - rtl8723bs_bt.bin				*[Unused as device uses rtk_hciattach driver]*
  - rtl8723bs_nic.bin
  - rtl8723bs_wowlan.bin		*[Unused as device does not support Wake on LAN]*


### Install
```
 make
 sudo make install
 sudo depmod -a
 sudo modprobe r8723bs
 
 ```
