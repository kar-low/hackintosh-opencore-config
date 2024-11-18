# hackintosh-opencore-config
---
##### computor
[![about this mac](./aboutMac.png)]
- **Motherboard** - B760M Pro RS/D4
    - **Audio**: Realtek ALC897 - AppleALC - ```alcid=98``` (config.plist  NVRAM $\rightarrow$ 7C436110-AB2A-4BBB-A880-FE41995C9F82 $\rightarrow$ boot-args)
    
    - **Network**: Dragon RTL8125BG - needs ```LucyRTL8125Ethernet.kext```
---
- **CPU** -  i7-13700k
- **GPU** - AMD Radeon RX 5600-XT
    - ```agdpmod=pikera``` boot-args needed (config.plist  NVRAM $\rightarrow$ 7C436110-AB2A-4BBB-A880-FE41995C9F82 $\rightarrow$ boot-args) 
- **SMBIOS** - MacPro7,1  (iMacPro1,1 giving blank screen after boot)
---

**Hide EFI boot option**
+ config.plist $\rightarrow$ Misc $\rightarrow$ Security $\rightarrow$ ScanPolicy = 17760515
---
**Skip boot picker**
+ config.plist $\rightarrow$ Misc $\rightarrow$ Boot $\rightarrow$ ShowPicker = False
---
**Tools**
- [ProperTree](https://github.com/corpnewt/ProperTree) - GUI plist editor
- [MountEFI](https://github.com/corpnewt/MountEFI) - EFI partition mount script
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) - Py script that uses acidanthera's macserial to generate SMBIOS and optionally saves them to a plist. 
