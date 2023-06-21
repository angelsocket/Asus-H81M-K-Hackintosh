# 👋 Hello! This is Hackintosh EFI for Asus H81M-K
![Banner](Banner.png)

## 🛠 Kexts
- Lilu
- WhateverGreen
- AppleALC
- NullEthernet
- NullEthernetInjector
- RealtekRTL8111
- SMCProccesor
- SMCSuperIO
- VirtualSMC

## 🖥 SMBIOS & Other
- Use iMac18.1 as SMBIOS | [Click to Download GenSMBIOS](https://https://github.com/corpnewt/GenSMBIOS)
- SIP 0x803 is already implemented in config.plist
- VGA Port not working! Use DVI-D

## 🔨 Patch iGPU
1. Download OCLP 0.6.7 after installation macOS on drive | [Click to download OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher/releases/tag/0.6.7)
2. Open OCLP
3. Click Post-Install Root Patch
4. Click Start Root Patching
5. Done! The computer will restart automatically

## 💖 Credits
- Apple for macOS
- Acidanthera team for OpenCore
- CorpNewt for GenSMBIOS
