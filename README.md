# 👋 Hello! This is Hackintosh EFI for Asus H81M-K
![Banner](Banner.png)

# 🛠 Kexts
- Lilu
- WhateverGreen
- AppleALC
- NullEthernet
- NullEthernetInjector
- RealtekRTL8111
- SMCProccesor
- SMCSuperIO
- VirtualSMC

# 🖥 SMBIOS & Other
- Use iMac18.1 as SMBIOS
- Use OCLP for patch GPU

- SIP 0x803 is already implemented in config.plist
- boot-args for install: -v keepsyms=1 debug=0x100 amfi_get_out_of_my_way=1

- VGA Port not working! Use DVI-D
- Chime sound working

# 💖 Credits
- Apple for macOS
- Acidanthera team for OpenCore
