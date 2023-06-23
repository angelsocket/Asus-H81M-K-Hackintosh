# Post Install

> ## 🪄 Patch iGPU
- Download OCLP 0.6.7 after installation macOS on drive | [Click to download OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher/releases/tag/0.6.7)
- Open OCLP
- Click Post-Install Root Patch
- Click Start Root Patching
- Done! The computer will restart automatically

> ## 🍎 Enable Apple Services (iMessage/iCloud/FaceTime)

- Download GenSMBIOS | [Click to download GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
- Open `GenSMBIOS.command`
- Type `1` to install MacSerial, then press ENTER.
- Type `3` to Generate SMBIOS, then press ENTER.
- Type `iMac18,1`, then press ENTER.
- Open `/EFI/OC/Config.plist` with any editor and navigate to `PlatformInfo -> Generic`
- Add the script's last result to `MLB, SystemSerialNumber and SystemUUID`

```diff
<key>PlatformInfo</key>
<dict>
  <key>Generic</key>
  <array>
    </dict>
      <key>AdviseFeatures</key>
      <false/>
      <key>MaxBIOSVersion</key>
      <false/>
      <key>MLB</key>
+     <string>00000000000000000</string>
      <key>ProcessorType</key>
      <integer>0</integer>
      <key>ROM</key>
      <data>ESIzRFVm</data>
      <key>SpoofVendor</key>
      <true/>
      <key>SystemMemoryStatus</key>
      <string>Auto</string>
      <key>SystemProductName</key>
      <string>iMac18,1</string>
      <key>SystemSerialNumber</key>
+     <string>000000000000</string>
      <key>SystemUUID</key>
+     <string>00000000-0000-0000-0000-000000000000</string>
      </dict>
   </array>
</dict>
```

- Save and reboot.

> ## 🔩 Disable verbose
- Mount EFI
- Open `/EFI/OC/Config.plist` with any editor and navigate to `NVRAM -> Add -> 7C436110-AB2A-4BBB-A880-FE41995C9F82`
- Change boot-args to the ones below

```diff
			</dict>
			<key>7C436110-AB2A-4BBB-A880-FE41995C9F82</key>
			<dict>
				<key>#INFO (prev-lang:kbd)</key>
				<string>en:252 (ABC), set 656e3a323532</string>
				<key>ForceDisplayRotationInEFI</key>
				<integer>0</integer>
				<key>SystemAudioVolume</key>
				<data>Rg==</data>
				<key>boot-args</key>
+				<string>alcid=53 amfi_get_out_of_my_way=0x1</string>
				<key>csr-active-config</key>
				<data>AwgAAA==</data>
				<key>prev-lang:kbd</key>
				<data></data>
				<key>run-efi-updater</key>
				<string>No</string>
			</dict>
```

> ## 📁 Extra
How mount EFI?
- Use `MountEFI` | [Click to download MountEFI](https://github.com/Andrej-Antipov/MountEFI/releases/tag/1.8)

Do I need to apply the iGPU patch again after a system update?
- Yes
