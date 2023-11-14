# linux58-tkg patches

- async_buffered_reads.mypatch - Implement true async buffered reads in io_uring; Incompatible with bcachefs - https://patchwork.kernel.org/cover/11571139/
- fsgsbase.mypatch - Patchset aiming at enhancing performance of Intel CPUs (ivybridge and up) - https://lore.kernel.org/patchwork/patch/1283965/
- mm_proactive_compaction.mypatch - https://patchwork.kernel.org/patch/11608611/
- PATCH-RFC-x86-mm-pat-Restore-large-pages-after-fragmentation.mypatch - Restore large pages that got fragmented, potentially improving performance marginally - https://patchwork.kernel.org/patch/11493785/
- The-new-cgroup-slab-memory-controller.mypatch - New cgroup slab memory controller by Roman Gushchin - https://patchwork.kernel.org/cover/11621221/
- workingset_protection.mypatch - Improve swapping/OOM behaviour - https://patchwork.kernel.org/cover/11680389/
- zstd.mypatch - Add support for Zstandard-compressed kernel (do not use for modules if you didn't apply kmod and mkinitcpio patches) - https://github.com/facebook/zstd/tree/dev/contrib/linux-kernel
- cachy-5.8.3.mypatch - Cachy CPU scheduler - **Requires selecting CFS** - https://github.com/hamadmarri/cachy-sched
