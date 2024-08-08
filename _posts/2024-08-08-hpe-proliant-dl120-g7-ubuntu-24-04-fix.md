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
GRUB_CMDLINE_LINUX_DEFAULT="quiet iommu=off intel_iommu=off intremap=off hpsa_simple_mode=1 hpsa_allow_any=1"
```

Save the file and run `update-grub` and reboot.