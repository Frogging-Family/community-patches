# linux516-tkg patches

- AMD_CPPC.mypatch - Adds AMD CPPC frequency management driver - https://git.kernel.org/pub/scm/linux/kernel/git/rui/linux.git/ NOTE: Support for most non-Epyc processors has been disabled by default. You can check by runing `lscpu | grep cppc`. If you get zero output, then you will need to add `amd_pstate.shared_mem=1` to your kernel parameters (via `/etc/default/grub` or similar)
- mglru_5.16.mypatch - Multigenerational LRU - https://linux-mm.googlesource.com/page-reclaim
- OpenRGB.mypatch - Patch to add OpenRGB compatibility for certain i2c controllers - https://gitlab.com/CalcProgrammer1/OpenRGB/-/blob/master/OpenRGB.patch
