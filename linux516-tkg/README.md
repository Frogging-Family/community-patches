# linux516-tkg patches

- AMD_CPPC.mypatch - Adds AMD CPPC frequency management driver - https://git.kernel.org/pub/scm/linux/kernel/git/rui/linux.git/ NOTE: Support for most non-Epyc processors has been disabled by default. You can check by runing `lscpu | grep cppc`. If you get zero output, then you will need to add `amd_pstate.shared_mem=1` to your kernel parameters (via `/etc/default/grub` or similar)
- lru_5.16.mypatch - Multigenerational LRU framework patchset, improving memory pressure handling - https://linux-mm.googlesource.com/page-reclaim - https://lore.kernel.org/lkml/20210520065355.2736558-1-yuzhao@google.com/
- OpenRGB.mypatch - Patch to add OpenRGB compatibility for certain i2c controllers - https://gitlab.com/CalcProgrammer1/OpenRGB/-/blob/master/OpenRGB.patch
- bt_hci_rcc_fix.mypatch - This fixes an annoying, but harmless, error message related to [BT controller not supporting HCI_READ_CODEC_CAPABILITIES](https://lore.kernel.org/all/DM8PR11MB55735DD3A1EA9132E1A71733F5499@DM8PR11MB5573.namprd11.prod.outlook.com/)
