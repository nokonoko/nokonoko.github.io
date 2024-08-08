---
layout: post
title:  "Fix HPE Proliant DL120 G7 to run on Ubuntu 24.04 LTS"
---

## The problem
When trying to run Ubuntu 24.04 LTS on a HPE Proliant DL120 G7 with a HP Smart Array P410 Controller for RAID
you might end up with the following errors, and a frozen boot.

![Ubuntu 24.04 error](https://blog.yeet.nu/img/2024-08-08-hpe-proliant-dl120-g7-ubuntu-24-04-fix/img-1.png)

```
DMAR: DRHD: handling fault status reg 3
DMAR: [DMA Read NO_PASID] Request device [04:00.0] fault addr XXXX PTE Read access
is not set
Buffer I/O error on device sdaX, logical block xxxxx
Buffer I/O error on device sdaX, lost async page write
```

## How to fix it
Boot into recovery on the previous kernel (5.15), or via a Live CD.

Edit `/etc/default/grub`, and change `GRUB_CMDLINE_LINUX_DEFAULT` to the following:
```
GRUB_CMDLINE_LINUX_DEFAULT="quiet iommu=off cciss_allow_hpsa=1 intremap=off hpsa_allow_any=1"
```

Save the file and run `update-grub` and reboot.


If you're also having the following issues with USB:
```
[   37.667766] usb 3-1: device not accepting address 15, error -11
[   37.667800] usb usb3-port1: attempt power cycle
[   37.791771] usb 3-1: new full-speed USB device number 16 using uhci_hcd
[   37.905762] usb 3-1: device descriptor read/64, error -11
[   38.125760] usb 3-1: device descriptor read/64, error -11
[   38.341784] usb 3-1: new full-speed USB device number 17 using uhci_hcd
[   38.455768] usb 3-1: device descriptor read/64, error -11
[   38.677775] usb 3-1: device descriptor read/64, error -11
[   38.779806] usb usb3-port1: unable to enumerate USB device
```

You can additionally add `usbcore.old_scheme_first=1`.