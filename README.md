# 👋 Hello! This is Hackintosh for Asus H81M-K
![Banner](Banner.png)
## ⚙️ Hardware
- Motherboard: ASUS H81M-K
- CPU: Intel Core i5 4570
- GPU: Intel HD Graphics 4600 (Patched using OCLP)
- RAM: 16GB 1600 DDR3 Kingston KVR16N11/8
- SSD: 120GB Samsung MZ7LN128HAHQ-000L2
- Sound: ALC887 (Layout: 53)

## 💾 Software
- Bootloader: OpenCore 0.9.3
- Patches: OCLP 0.6.7
- macOS: Ventura 13.4.1
- BIOS: 3604

## 📃 What works and what doesn't

<details>
<summary><strong> Click to open! </strong></summary>
<br>
  
> ### Hardware

- 🟢 - Fully working
- 🟠 - Partially working
- 🔴 - Not working

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| Graphics (HD 4600)                   | 🟢  | `WhateverGreen.kext` & OCLP 0.6.7 |
| Sound (ALC887)                       | 🟢  | `AppleALC.kext` & alcid=53 |
| USB Ports                            | 🟢  | Native |
| Ethernet                             | 🟢  | `RealtekRTL8111.kext` | 
| Sleep                                | 🟢  | Working |
| VGA Port                             | 🔴  | Not Working |

> ### macOS Continuity

| Feature                              | Status | Dependency          |
| :----------------------------------- | ------ | ------------------- |
| iCloud, iMessage, FaceTime           | 🟢   | Whitelisted Apple ID, Valid SMBIOS  |
| Time Machine                         | 🟢   | Native  |
| AirDrop                              | 🟠   | Needed WiFi and Bluetooth  |
</details>

## 🎛 BIOS Settings
- Install latest BIOS 3604 | [Click to download BIOS](https://www.asus.com/supportonly/h81m-k/helpdesk_bios/)
- Reset BIOS to default and check this settings:

<details>
<summary><strong> Click to open! </strong></summary>
<br>
  
> ### BIOS Settings

| Setting                              | Option |
| :----------------------------------- | ------ |
| CSM                                  | Disabled |
| iGPU Memory                          | 96MB |
| CPU MSR Lock                         | Disabled |
| Sata Configuration                   | AHCI | 
| USB Mode                             | Smart Auto |
| VGA Port                             | Disabled |
| Secure Boot                          | Other OS |
</details>

## 🖥 SMBIOS & Other
- Use iMac18.1 as SMBIOS | [Click to Download GenSMBIOS](https://https://github.com/corpnewt/GenSMBIOS)
- SIP 0x803 is already implemented in config.plist
  
## 💽 Installation macOS
- Instructions coming soon!

## 🪄 Patch iGPU
1. Download OCLP 0.6.7 after installation macOS on drive | [Click to download OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher/releases/tag/0.6.7)
2. Open OCLP
3. Click Post-Install Root Patch
4. Click Start Root Patching
5. Done! The computer will restart automatically

## 💖 Credits
- Apple for macOS
- Acidanthera team for OpenCore
- CorpNewt for GenSMBIOS
