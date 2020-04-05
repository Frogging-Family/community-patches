# mesa-git patches

- bias_shadows_radv_dxvk.mymesapatch : Fixes some shadow rendering issues with RADV - ! Not compatible with VK_JOSH_depth_bias patches ! (https://bugs.freedesktop.org/show_bug.cgi?id=109599)
- intel_haswell_vk_workaround.mymesarevert : Reverts https://gitlab.freedesktop.org/mesa/mesa/commit/7c1b39cf18481f0d15f3ffb1130da4479032d76a to workaround visual breakage on haswell and older iGPUs with vulkan
- VK_JOSH_depth_bias_info_radv.mymesapatch : Adds VK_JOSH_depth_bias_info extension for use with D9VK (fixes shadows rendering in various cases)
- VK_JOSH_depth_bias_info_header.mymesapatch : VK_JOSH_depth_bias_info extension header, dependency for the above patch
- 8_16bitstorage_aco_forceenable.mymesapatch : Force enable VK_KHR_8bit_storage, VK_KHR_16bit_storage and shaderInt8 on ACO (it's unfinished, so be aware of potential issues) - Most useful for Doom Eternal and Yuzu - https://gitlab.freedesktop.org/daniel-schuermann/mesa/-/commits/storage8bit_test
- mhw-revert.mymesapatch : Reverts https://gitlab.freedesktop.org/mesa/mesa/-/commit/507956ed04fcdcfd44419d1b16f032e1d81d0dcb to fix Monster Hunter World crashing either on launch (populated mesa shader cache/DXVK's state cache) or on main menu transition (cold caches).
