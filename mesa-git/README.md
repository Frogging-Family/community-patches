# mesa-git patches

- bias_shadows_radv_dxvk.mymesapatch : Fixes some shadow rendering issues with RADV - ! Not compatible with VK_JOSH_depth_bias patches ! (https://bugs.freedesktop.org/show_bug.cgi?id=109599)
- intel_haswell_vk_workaround.mymesarevert : Reverts https://gitlab.freedesktop.org/mesa/mesa/commit/7c1b39cf18481f0d15f3ffb1130da4479032d76a to workaround visual breakage on haswell and older iGPUs with vulkan
- VK_JOSH_depth_bias_info_radv.mymesapatch : Adds VK_JOSH_depth_bias_info extension for use with D9VK (fixes shadows rendering in various cases)
- VK_JOSH_depth_bias_info_header.mymesapatch : VK_JOSH_depth_bias_info extension header, dependency for the above patch
- d3d9_legacy_opcodes.mymesapatch : Workaround for some rendering issues in some d3d9 games such as Bayonetta when using DXVK - RADV_PERFTEST=mulzerowins to force this behaviour, to be used with d3d9.floatEmulation = false in DXVK - https://gitlab.freedesktop.org/JoshuaAshton/mesa/-/commits/aco-d3d9
- aco_default.mymesapatch : Patch to enable ACO by default on RADV, from Daniel Schuermann's repo - https://github.com/daniel-schuermann/mesa/commit/ace9c8fb59b09bf6e16bcfdfafcc2a4510a98783
