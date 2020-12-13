# linux510-tkg patches

- RDTSC-KVM-Handler.mypatch - Spoofs the RDTSC instruction in KVM, making the VM exit undetected - https://github.com/WCharacter/RDTSC-KVM-Handler
- futex2_interface.mypatch - Adds support for experimental futex2 interface - Can be used by Wine/Proton's Fsync - *Requires a patched wine/proton : https://github.com/Frogging-Family/community-patches/tree/master/wine-tkg-git/fsync_futex2.mypatch* - https://gitlab.collabora.com/tonyk/linux/-/tree/futex2-stable
