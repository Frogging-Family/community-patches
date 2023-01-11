# linux61-tkg patches

- OpenRGB.mypatch - Patch to add OpenRGB compatibility for certain i2c controllers - https://gitlab.com/CalcProgrammer1/OpenRGB/-/blob/master/OpenRGB.patch
- x86_split_lock-Add_sysctl_to_control_the_misery_mode.mypatch - Allows controlling the "misery mode" behavior, for which the default changed with b041b525dab9 ("x86/split_lock: Make life miserable for split lockers"), notably slowing down some windows games runnning through Wine - We are enforcing the behavior to "off" in linux-tkg through kernel command line, but this makes it configurable at runtime -  https://lore.kernel.org/all/20221024200254.635256-1-gpiccoli@igalia.com/
- BBRv2.mypatch - Add BBRv2 TCP IPv4 algorithm - https://github.com/google/bbr/tree/v2alpha - Imported from https://codeberg.org/pf-kernel/linux
