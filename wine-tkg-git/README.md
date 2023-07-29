# wine-tkg-git and proton-tkg patches

**More userpatches for wine-tkg are also made available by @openglfreak : https://github.com/openglfreak/wine-tkg-userpatches**

*Thank you!*

### Wine/Proton-tkg-git will auto-clone this repo two dirs up from their buildscript dir (`../../community-patches`) if valid community patches are found in their .cfg file (`_community_patches=""` array).
### Alternatively, you can also clone this repo by hand next to the `wine-tkg-git` root dir (the one containing both `wine-tkg-git` and `proton-tkg` dirs) so the build system sees it - `git clone https://github.com/Frogging-Family/community-patches.git`.


## Proton patches
- amdags.mypatch : Add amdags dll (proton patch - wine version to apply to a wine-tkg build)
- amdags-proton.mypatch : Add amdags dll (proton patch - proton version to apply to a proton-tkg build)
- atiadlxx-proton.mypatch : Add atiadlxx stub dll for Blackops 3, Shadow of War and friends (proton patch - proton version to apply to a proton-tkg build - Requires `_msvcrt_nativebuiltin="true"`)
- hide-prefix-update-window.mypatch : As the name implies, will hide the prefix update dialog - https://github.com/ValveSoftware/wine/commit/6051b0612ca0436139f6e059cdaa704b7d9fa7ab - Doesn't apply to proton-tkg (already included)
- unhide-prefix-update-window.mypatch : As the name implies, will unhide the prefix update dialog - https://github.com/ValveSoftware/wine/commit/6051b0612ca0436139f6e059cdaa704b7d9fa7ab - Applies to proton-tkg **only**
- winex11-fs-no_above_state.mypatch : Don't set ABOVE state for FULLSCREEN windows, fixing alt-tabbing in various games. There's a reported issue with Xfce where panels can stay above games with this patch applied. Requires `_proton_fs_hack="true"` in your .cfg - https://github.com/ValveSoftware/wine/commit/a8675091927c01a0c28de349517c5010557f06a9
- winex11-fs-no_above_state-nofshack.mypatch : Same as above for `_proton_fs_hack="false"` or wine 5.20 or newer - Thanks to ErdeFB - https://github.com/Frogging-Family/community-patches/issues/31
- 0002-proton_QPC.mypatch : Rémi Bernon's Qpc timer bypass patchset - Improves timing and performance in various games
- winex11drv-cache-clip-window-staging.mypatch : Paul Gofman's attempt at fixing mouse capture issues and reducing overhead when using high DPI mice - Rebased by FuzzyQuils - https://github.com/ValveSoftware/wine/commit/b23d6802e3e2437be2a2d1cbc1d358fd336fc8d3


## Game-specific
- legoisland_168726.mypatch : Add functions needed by, notably, lego island - https://bugs.winehq.org/show_bug.cgi?id=10729
- FinalFantasyXVHack.mypatch : Hack enabling Final Fantasy XV Steam to run - https://github.com/ValveSoftware/Proton/issues/74#issuecomment-553084621
- MWSE_hack.mypatch : Hack to allow Morrowind Script Extender to work - https://bugs.winehq.org/show_bug.cgi?id=47940#c24
- blackops2_unhandled_exception_fix.mypatch : Fix for the Unhandled Exception crash of Call of Duty - Black Ops 2 on start up - Won't work on Proton due to CEG - https://bugs.winehq.org/show_bug.cgi?id=46472
- NFSWLauncherfix.mypatch : Fix for Need for Speed World's SBRW launcher - https://github.com/SoapboxRaceWorld/wine
- gta4_gamepad_workaround.mypatch : Workaround for GTA IV gamepad issues thanks to @AlexeyProkhin - https://github.com/ValveSoftware/Proton/issues/350#issuecomment-606425633
- 0001-powershell-add-wrapper-for-powershell-using-Powershe.mypatch - Patch for Waves Central from Louis Lenders (requires winetricks arial) - https://github.com/Frogging-Family/community-patches/pull/20
- star-citizen-StorageDeviceSeekPenaltyProperty.mypatch - Patch to add StorageDeviceSeekPenaltyProperty support, needed by StarCitizen 3.13+ PTU - https://bugs.winehq.org/show_bug.cgi?id=50992
- mass_effect_legendary_psapi.mypatch - Patch to allow Mass Effect Legendary edition to run - https://github.com/ValveSoftware/Proton/issues/4823#issuecomment-841587666 - Regarding other things needed for the game, see https://github.com/ValveSoftware/Proton/issues/4823#issuecomment-841761975
- mfplat_nv12_d3d11_buffers.mypatch - Patch by Adrian | cooltyp100 (VKx) to fix Nier: Replicant videos having a green tint - Thanks!
- roblox_fix.mypatch - Fixes an issue with VMProtect, allowing Roblox to run - Patch by Kalen Alwardt - https://bugs.winehq.org/show_bug.cgi?id=39142
- roblox_mouse_fix.mypatch - Fixes the mouse cursor getting stuck in Roblox
- roblox_mouse_fix-fshack.mypatch - Same as above, but compatible with proton's FS hack - Thanks to rezzafr33 on Discord
- unprivileged_ICMP.mypatch - Notably fixes missing ping in BF4 (which could lead to kicks on some servers) - https://source.winehq.org/patches/data/207990
- EA_desktop_fix.mypatch - Allows EA desktop to run - Patch by Esdras Tarsis - https://bugs.winehq.org/show_bug.cgi?id=49887
- ffxiv_mac.mypatch : Add support for using Final Fantasy XIV with Mac authentication (without HideWineExports)
- RtlCreateTimer_fix.mypatch: Fix race condition in RtlCreateTimer - affect Guild Wars 2 with Arcdps (no other cases known yet). Since aug.28.2021 there is a temporary workaround on the Arcdps side (just some extra delays have been added, but this may not work for specific hardware) until https://bugs.winehq.org/show_bug.cgi?id=51683 is resolved.
- persona-5-royal_transacted-file-APIs.mypatch - Fixes Persona 5 Royal save functionality - https://gitlab.winehq.org/wine/wine/-/merge_requests/1145

## Misc
- 0001-rockstarlauncher_install_fix.mypatch : Fix for rockstar launcher installer crashing - https://github.com/ValveSoftware/wine/commit/e485252dfad51a7e463643d56fe138129597e4b6 - Doesn't apply to proton-tkg or wine builds using `_protonify="true"` (already included)
- 0001-rockstarlauncher_downloads.mypatch : Hack to workaround failing downloads with rockstar launcher - https://bugs.winehq.org/show_bug.cgi?id=47843 - Doesn't apply to proton-tkg or wine builds using `_protonify="true"` (already included)
- origin_downloads_e4ca5dbe_revert.mypatch : Workaround for Origin client game downloading issues - https://bugs.winehq.org/show_bug.cgi?id=48032
- 0001-Add-some-semi-stubs-in-user32.mypatch : Fixes black/green screen when running Steep in fullscreen/windowed fullscreen mode, courtesy of Guy1524
- winex11_limit_resources-nmode.mypatch : Hack to fix DARK SOULS III, Nier: Automata and Sekiro: Shadows Die Twice crashing when there are too many display modes available - This can lead to missing modes on other games if you're affected by the issue - https://github.com/ValveSoftware/wine/pull/83
- 0001-Allow-RtlSizeHeap-to-check-pointers-from-GlobalLock-mainline.mypatch : HeapSize/RtlHeapSize can operate on GMEM_MOVEABLE GlobalAlloc/LocalAlloc locked pointers. Resolve crashing issues with wxWidgets drag and drop. Fix Wrye Bash (pre-310), DO NOT breaks Dotnet40 installation.  This is another fix for - https://bugs.winehq.org/show_bug.cgi?id=38924 . For  Wine mainline
- 0001-Allow-RtlSizeHeap-to-check-pointers-from-GlobalLock-staging.mypatch : HeapSize/RtlHeapSize can operate on GMEM_MOVEABLE GlobalAlloc/LocalAlloc locked pointers. Resolve crashing issues with wxWidgets drag and drop. Fix Wrye Bash (pre-310), DO NOT breaks Dotnet40 installation.  This is another fix for - https://bugs.winehq.org/show_bug.cgi?id=38924 . For Wine Staging Heap Patchset
- 0003-Allow-RtlSizeHeap-to-check-pointers-from-GlobalLock-LFH.mypatch : HeapSize/RtlHeapSize can operate on GMEM_MOVEABLE GlobalAlloc/LocalAlloc locked pointers. Resolve crashing issues with wxWidgets drag and drop. Fix Wrye Bash (pre-310), DO NOT breaks Dotnet40 installation.  This is another fix for - https://bugs.winehq.org/show_bug.cgi?id=38924 . For 0002-Proton-LFH patchset
- shell32-Move-file-SHFileOperation-allow-from-wildchar-move.mypatch : Allow wildchar FO_MOVE to execute even if the source is only 1 file. Needed fo FX Interactive Store - https://bugs.winehq.org/show_bug.cgi?id=39269
- ID3DXEffectCompiler-partial-implementation.mypatch : Partial implementation of ID3DXeffectCompiler interface. Avoid Oblivion Reloaded and maybe other applications needeing a native d3dx9_xx.dll to compile effects. Require native d3dcompiler_xx.dll - https://bugs.winehq.org/show_bug.cgi?id=46779
- ntdll_Map_top-down_if_dll_characteristics_include_DYNAMIC_BASE.mypatch : Fix for SKSE64, thanks to @qsniyg - https://bugs.winehq.org/show_bug.cgi?id=44893 - https://bugs.winehq.org/show_bug.cgi?id=48641
- wine-fix-gcc10.mypatch - Fix for a specific compilation error (`error: unknown type name ‘va_list’`) some people encounter for unknown reason - https://github.com/Frogging-Family/wine-tkg-git/issues/165 - Thanks to @drizzt https://gist.github.com/drizzt/364a915fc5f88b6143b913e7f494950b
- Don-t-Skip-adding-public-symbols-Required-for-FakePDB.mypatch : Allow FakePDB  generated or LLVM generated PDBs to works with the builtin dbghelp.dll 
- Shell32-CreateDirectoryInDestinationInFileOp-Move-multiop.mypatch : Fix Multiop fileop MOVE not creating directories in destination. Required for WryeBash Installer functionality - Thanks to @t0suj4
- Add-SORT_DIGITSAS-UMBERS-flag-to-CompareStringsEx.mypatch : Fix for FL Studio 20.8 crash on startup - https://bugs.winehq.org/show_bug.cgi?id=50362
- 0001-ntdll-Use-kernel-soft-dirty-flags-for-write-watches-.mypatch : Needed for D3D12 APITracing - Needs a patched kernel (see linux-tkg)
- wine_wayland_driver.mypatch : Adds experimental Wayland driver by Alexandros Frantzis - https://www.winehq.org/pipermail/wine-devel/2021-June/188412.html - https://gitlab.collabora.com/alf/wine/-/tree/wayland - Requires you to start wine with `DISPLAY= WAYLAND_DISPLAY=wayland-0` (wayland-0 being your desired wayland output)
- amd_fsr_fshack.mypatch : Replaces Proton FS hack's linear filtering with AMD FidelityFX super resolution - Thanks to dadschoorse - Kinda experimental/WIP, it might not work on all games. Depends on `_use_staging="true"` and `_proton_fs_hack="true"` in your cfg - Enable with
`WINE_FULLSCREEN_FSR=1` env var, and tweak sharpening amount with `WINE_FULLSCREEN_FSR_STRENGTH=5` (5 is default sharpening, lower numbers mean more sharpening, 0 is max sharpening) - https://github.com/DadSchoorse/wine-proton/commits/fsr-clean
- amd_fsr_fshack-alternative.mypatch : Variation of the above fsr implementation with additions from GloriousEggroll to workaround the problem of missing resolutions when too many are available in some games/displays configurations - See https://github.com/GloriousEggroll/proton-ge-custom/releases/tag/GE-Proton7-24 for how to enable/use.
- proton_winex11_Let_the_WM_focus_our_windows_by_default.mypatch : Proton patch that is supposed to fix game windows not being in focus when first started and when exiting, which can cause surprising keyboard behavior (e.g. accidentally Alt-F4ing Steam itself, which is in the background). However, it breaks some apps (see https://github.com/Frogging-Family/wine-tkg-git/issues/466) while being seemingly not needed with most DEs.
- revert_return_correct_color_depth_for_display_DCs_in_GetDeviceCaps.mypatch : Fixes issue where some users with Nvidia GPUs and multi-monitor setups using DVI see Xorg pin their CPU to 100% usage whenever using Wine after upstream commit d171d11 - https://bugs.winehq.org/show_bug.cgi?id=51420
- server-Enable-link-time-optimization.mypatch : Enables LTO for wineserver
- 0001-actctx-Use-build_assembly_dir-to-assign-a-directory.mypatch : Allow some applications to properly find some assemblies.
- 0001-Allow-revocation-check-to-use-the-net.mypatch : Some application that use CERT_VERIFY_CACHE_ONLY_BASED_REVOCATION in bitwise OR with other flags need a full net revocation check. Rustup is affected
- 0001-Revert-server-Handle-the-entire-IOCTL_AFD_POLL-ioctl.mypatch : Revert the commit that moved IOCTL_AFD_POLL serverside. Rustup (and possible other application that use this routine) need this revert to properly park/unpark the thread.
- win32-Initialize-params-for-WndProc-after-WH_CALLWNDPROC.mypatch : Initalize parameters for WndProc procedure after WH_CALLWNDPROC hook is called. (Required )
- 0001-Force-full-erase-when-WM_PAINT-in-LVS_EX_DOUBLEBUFFE.mypatch : Force a background erase on LVS_EX_DOUBLEBUFFERED listviews. Fix black background for listviews on some apps.
- VisualStudio2019_patches.mypatch : A series of patches for a working installation of Visual Studio 2019
- Proper_refcount_forwarded_exports.mypatch : Allow forwarded exports to properly tracks their refcounts, avoiding spuruious DLL unloading. Needed for IDA Pro IDAPython3 