# linux59-tkg patches

- OpenRGB.mypatch - Patch to add OpenRGB compatibility for certain i2c controllers - https://gitlab.com/CalcProgrammer1/OpenRGB/-/blob/master/OpenRGB.patch
- PATCH-RFC-x86-mm-pat-Restore-large-pages-after-fragmentation.mypatch - Restore large pages that got fragmented, potentially improving performance marginally - https://patchwork.kernel.org/patch/11493785/
- cachy-5.9-r9.mypatch - Cachy CPU scheduler - **Requires selecting CFS** - https://github.com/hamadmarri/cacule-cpu-scheduler/tree/master/patches/Cachy/v5.9
- cacule-5.9.mypatch - CacULE CPU scheduler - **Requires selecting CFS** - https://github.com/hamadmarri/cacule-cpu-scheduler/tree/master/patches/CacULE/v5.9
- zstd.mypatch - Add support for Zstandard-compressed modules - https://github.com/facebook/zstd/tree/dev/contrib/linux-kernel - Thanks to veganvelociraptor https://github.com/Frogging-Family/community-patches/issues/30
- RDTSC-KVM-Handler.mypatch - Spoofs the RDTSC instruction in KVM, making the VM exit undetected - https://github.com/WCharacter/RDTSC-KVM-Handler
