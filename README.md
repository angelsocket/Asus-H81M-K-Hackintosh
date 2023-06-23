# 👋 Hello! This is Hackintosh for Asus H81M-K
![Banner](Files/Banner.png)
## ⚙️ Hardware
- Motherboard: ASUS H81M-K
- CPU: Intel Core i5 4570
- GPU: Intel HD Graphics 4600 (Patched using OCLP)
- RAM: 16GB 1600 DDR3 Kingston KVR16N11/8
- SSD: 120GB Samsung MZ7LN128HAHQ-000L2

## 💾 Software
- Bootloader: OpenCore 0.9.3
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
| Sleep                                | 🟢  | Native |
| VGA Port                             | 🔴  | Does not exist on real apple computers |

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
  
## 💽 Installation macOS
- [**Dortania's OpenCore Install Guide**](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/): Creating a macOS installer

## 🪄 Post Install
- [**ReadMe Post Install**](/Files/PostInstall.md): Requirements before installing.

## 💖 Credits
- Apple for macOS
- Acidanthera team for OpenCore
- CorpNewt for GenSMBIOS
