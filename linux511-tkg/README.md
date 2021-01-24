# linux511-tkg patches
- bluetooth-next.mypatch - Adds all upstream commits from bluetooth-next - https://git.kernel.org/pub/scm/linux/kernel/git/bluetooth/bluetooth-next.git

- bpf.mypatch - Fixes BPF/BTF handling for modules with missing BPF records, which is currently still a lot of them, including the NLS modules. Really, 5.11 is not terribly usable without this.

- futex2_interface.mypatch - Adds support for experimental futex2 interface - Can be used by Wine/Proton's Fsync - *Requires a patched wine/proton : https://github.com/Frogging-Family/community-patches/tree/master/wine-tkg-git/fsync_futex2.mypatch* - https://gitlab.collabora.com/tonyk/linux/-/tree/futex2-dev
