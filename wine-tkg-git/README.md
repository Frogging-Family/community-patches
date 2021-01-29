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


## Game-specific
- legoisland_168726.mypatch : Add functions needed by, notably, lego island - https://bugs.winehq.org/show_bug.cgi?id=10729
- FinalFantasyXVHack.mypatch : Hack enabling Final Fantasy XV Steam to run - https://github.com/ValveSoftware/Proton/issues/74#issuecomment-553084621
- MWSE_hack.mypatch : Hack to allow Morrowind Script Extender to work - https://bugs.winehq.org/show_bug.cgi?id=47940#c24
- blackops2_unhandled_exception_fix.mypatch : Fix for the Unhandled Exception crash of Call of Duty - Black Ops 2 on start up - Won't work on Proton due to CEG - https://bugs.winehq.org/show_bug.cgi?id=46472
- NFSWLauncherfix.mypatch : Fix for Need for Speed World's SBRW launcher - https://github.com/SoapboxRaceWorld/wine
- gta4_gamepad_workaround.mypatch : Workaround for GTA IV gamepad issues thanks to @AlexeyProkhin - https://github.com/ValveSoftware/Proton/issues/350#issuecomment-606425633
- 0001-powershell-add-wrapper-for-powershell-using-Powershe.patch - Patch for Waves Central from Louis Lenders (requires winetricks arial) - https://github.com/Frogging-Family/community-patches/pull/20


## Misc
- rockstarlauncher_install_fix.mypatch : Fix for rockstar launcher installer crashing - https://github.com/ValveSoftware/wine/commit/e485252dfad51a7e463643d56fe138129597e4b6 - Doesn't apply to proton-tkg or wine builds using `_protonify="true"` (already included)
- rockstarlauncher_downloads.mypatch : Hack to workaround failing downloads with rockstar launcher - https://bugs.winehq.org/show_bug.cgi?id=47843 - Doesn't apply to proton-tkg or wine builds using `_protonify="true"` (already included)
- origin_downloads_e4ca5dbe_revert.mypatch : Workaround for Origin client game downloading issues - https://bugs.winehq.org/show_bug.cgi?id=48032
- 0001-Add-some-semi-stubs-in-user32.mypatch : Fixes black/green screen when running Steep in fullscreen/windowed fullscreen mode, courtesy of Guy1524
- winex11_limit_resources-nmode.mypatch : Hack to fix DARK SOULS III, Nier: Automata and Sekiro: Shadows Die Twice crashing when there are too many display modes available - This can lead to missing modes on other games if you're affected by the issue - https://github.com/ValveSoftware/wine/pull/83
- kernel32-implement-Windows-NT-style-GMEM_MOVEABLE-LM-no-staging.mypatch : Allow GlobalAlloc and LocalAlloc GMEM_MOVEABLE to be used with HeapSize. Resolve crashing issues with wxWidgets drag and drop. Fix Wrye Bash (for non staging build ) - https://bugs.winehq.org/show_bug.cgi?id=38924
- kernel32-implement-Windows-NT-style-GMEM_MOVEABLE-LM-staging.mypatch : Allow GlobalAlloc and LocalAlloc GMEM_MOVEABLE to be used with HeapSize. Resolve crashing issues with wxWidgets drag and drop. Fix Wrye Bash (for staging build ) - https://bugs.winehq.org/show_bug.cgi?id=38924
- shell32-Move-file-SHFileOperation-allow-from-wildchar-move.mypatch : Allow wildchar FO_MOVE to execute even if the source is only 1 file. Needed fo FX Interactive Store - https://bugs.winehq.org/show_bug.cgi?id=39269
- ID3DXEffectCompiler-partial-implementation.mypatch : Partial implementation of ID3DXeffectCompiler interface. Avoid Oblivion Reloaded and maybe other applications needeing a native d3dx9_xx.dll to compile effects. Require native d3dcompiler_xx.dll - https://bugs.winehq.org/show_bug.cgi?id=46779
- ntdll_Map_top-down_if_dll_characteristics_include_DYNAMIC_BASE.mypatch : Fix for SKSE64, thanks to @qsniyg - https://bugs.winehq.org/show_bug.cgi?id=44893 - https://bugs.winehq.org/show_bug.cgi?id=48641
- fsync_futex2.mypatch - Add support for experimental futex2 interface for Fsync. Can be disabled to use regular fsync exporting `WINEFSYNC_FUTEX2=0`. Requires `_use_fsync="true"` *This requires a patched kernel in order to work : https://github.com/Frogging-Family/community-patches/tree/master/linux510-tkg/futex2_interface.mypatch* - https://gitlab.collabora.com/tonyk/wine/-/tree/proton_5.13 - https://github.com/ValveSoftware/wine/commits/experimental_5.13
- wine-fix-gcc10.mypatch - Fix for a specific compilation error (`error: unknown type name ‘va_list’`) some people encounter for unknown reason - https://github.com/Frogging-Family/wine-tkg-git/issues/165 - Thanks to @drizzt https://gist.github.com/drizzt/364a915fc5f88b6143b913e7f494950b
