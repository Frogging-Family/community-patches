# linux61-tkg patches

- x86_split_lock-Add_sysctl_to_control_the_misery_mode.mypatch - Allows controlling the "misery mode" behavior, for which the default changed with b041b525dab9 ("x86/split_lock: Make life miserable for split lockers"), notably slowing down some windows games runnning through Wine - We are enforcing the behavior to "off" in linux-tkg through kernel command line, but this makes it configurable at runtime -  https://lore.kernel.org/all/20221024200254.635256-1-gpiccoli@igalia.com/
- BBRv2.mypatch - Add BBRv2 TCP IPv4 algorithm - https://github.com/google/bbr/tree/v2alpha - Imported from https://codeberg.org/pf-kernel/linux
- cap_sys_nice_begone.mypatch - Allow all applications to request high priority queues in AMDGPU. Allows SteamVR to use Asynchronous Reprojection on Flatpak and NixOS - From https://codeberg.org/Scrumplex/flake
