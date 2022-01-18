# linux514-tkg patches

- OpenRGB.mypatch - Patch to add OpenRGB compatibility for certain i2c controllers - https://gitlab.com/CalcProgrammer1/OpenRGB/-/blob/master/OpenRGB.patch
- AMD_CPPC.mypatch - Adds AMD CPPC frequency management driver - http://lkml.iu.edu/hypermail/linux/kernel/2109.1/00542.html NOTE: Support for most non-Epyc processors has been disabled by default. You can check by runing `lscpu | grep cppc`. If you get zero output, then you will need to add `amd_pstate.shared_mem=1` to your kernel parameters (via `/etc/default/grub` or similar)
- AMD_fix_max_memory_clock.mypatch - Fixes an issue in AMD GPU driver locking memory clocks at maximum speed for Radeon RX cards - https://gitlab.freedesktop.org/drm/amd/-/issues/1709
- lru_5.14.mypatch - multigenerational LRU framework patchset, improving memory pressure handling - https://lore.kernel.org/lkml/20210520065355.2736558-1-yuzhao@google.com/
