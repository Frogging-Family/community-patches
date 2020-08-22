# linux57-tkg patches

- async_buffered_reads.mypatch - Implement true async buffered reads in io_uring; Incompatible with bcachefs - https://patchwork.kernel.org/cover/11571139/
- fgsgsbase.mypatch - Patchset aiming at enhancing performance of Intel CPUs (ivybridge and up) - https://lkml.org/lkml/2020/5/28/1358
- mm_proactive_compaction.mypatch - https://lkml.org/lkml/2019/10/30/1076
- OpenRGB.mypatch - Patch to add OpenRGB compatibility for certain i2c controllers - https://gitlab.com/CalcProgrammer1/OpenRGB/-/blob/master/OpenRGB.patch
- PATCH-RFC-x86-mm-pat-Restore-large-pages-after-fragmentation.mypatch - Restore large pages that got fragmented, potentially improving performance marginally - https://patchwork.kernel.org/patch/11493785/
- Reduce-lock-contention-on-swap-cache-from-swap-slots-allocation.mypatch - Reduces lock contention when swapping, may help performance on out-of-memory - https://patchwork.kernel.org/patch/11577407/
- The-new-cgroup-slab-memory-controller.mypatch - New cgroup slab memory controller by Roman Gushchin - https://patchwork.kernel.org/cover/11574017/
- workingset_protection.mypatch - Improve swapping/OOM behaviour - https://patchwork.kernel.org/cover/11609035/
- zstd.mypatch - Add support for Zstandard-compressed kernel (do not use for modules if you didn't apply kmod and mkinitcpio patches) - https://github.com/facebook/zstd/tree/dev/contrib/linux-kernel
