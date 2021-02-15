# linux511-tkg patches
- bluetooth-next.mypatch - Adds all upstream commits from bluetooth-next - https://git.kernel.org/pub/scm/linux/kernel/git/bluetooth/bluetooth-next.git

- futex2_interface.mypatch - Adds support for experimental futex2 interface - Can be used by Wine/Proton's Fsync - Requires `_config_expert="true"` - *Requires a patched wine/proton : https://github.com/Frogging-Family/community-patches/tree/master/wine-tkg-git/fsync_futex2.mypatch* - https://gitlab.collabora.com/tonyk/linux/-/tree/futex2-dev
