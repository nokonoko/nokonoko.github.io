---
layout: post
title:  "Fix HPE ProLiant DL120 G7 to run on Ubuntu 24.04 LTS"
---

## The problem
When trying to run Ubuntu 24.04 LTS on a HPE ProLiant DL120 G7 server with a HP Smart Array P410 Controller for RAID
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
1. Hold shift before the Ubuntu boot starts, in the advanced Grub menu hover over your current kernel and hit `e`, find the section with something similar to this:
   ```
   linux   /vmlinuz-6.8.1-1005-realtime root=UUID=51e99cc3-1a4f-4aa7-be3c-1a793d20eff5 ro  quiet splash
   ```
2. And modify it to something like this:
   ```
   linux   /vmlinuz-6.8.1-1005-realtime root=UUID=51e99cc3-1a4f-4aa7-be3c-1a793d20eff5 ro  quiet splash iommu=off cciss_allow_hpsa=1 intremap=off hpsa_allow_any=1
   ```
3. Hit `CTRL+X` to boot with those parameters.
4. Once booted we need to make these changes permanent by editing `/etc/default/grub`, and change `GRUB_CMDLINE_LINUX_DEFAULT` to the following:
   ```
   GRUB_CMDLINE_LINUX_DEFAULT="quiet iommu=off cciss_allow_hpsa=1 intremap=off hpsa_allow_any=1"
   ```
5. Save the file and run `update-grub` and then reboot.

## Possible USB issues
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