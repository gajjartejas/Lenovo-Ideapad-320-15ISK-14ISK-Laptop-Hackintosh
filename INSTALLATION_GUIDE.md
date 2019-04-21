# Installation guide for Lenovo-Ideapad-320-15ISK-14ISK-Laptop-Hackintosh

## Requirements
 - Active internet connection and Apple Mac
 - USB Stick minimum 8GB
 - Mac OS High Sierria or Mac OS Mojave should be already downloaded
 
## Tools required
 - xCode or any Plist editor
 - [Clover Configurator](https://mackie100projects.altervista.org/download-clover-configurator/)
 - [UniBeast - Mojave](https://www.tonymacx86.com/resources/unibeast-9-2-0-mojave.426/)
 
 First use UniBeast-Mojave to create bootable USB drive. It will take some time after finished make a sure EFI Folder is mounted. Now download [config_HD5000_5100_5200.plist](https://github.com/RehabMan/OS-X-Clover-Laptop-Config/blob/master/config_HD515_520_530_540.plist) from https://github.com/RehabMan/OS-X-Clover-Laptop-Config and save it and open it with Clover Configurator. 
 
 ## Fix Audio
 Use [AppleALC](https://github.com/acidanthera/AppleALC) and download kext. Place AppleALC.kext on EFI/CLOVER/kexts/Other folder
 
 You need to edit plist for working audio below is stpe:
 Go to Clover Configurator->Boot->Arguments add `nv_disable=1`
 Now go to Clover Configurator->Devices->Audio->Inject add audio id `20` and check ResetHDA
 
  ## Fix Graphics
  Currently NVIDIA graphics not working so you need to use Intel hd 520 for this.
  
  You need to download [Lilu kext](https://github.com/acidanthera/Lilu) place Lilu.kext on EFI/CLOVER/kexts/Other folder. You also need to download [WhateverGreen kext](https://github.com/acidanthera/whatevergreen) to work intel hd graphics place WhateverGreen.kext in EFI/CLOVER/kexts/Other folder
  
  You need to edit plist as below:
  Go to Clover Configurator->Devices->Devices*
  
  select `PciRoot(0)/Pci(0x1f,3)` now delete all properties keys and add `layout-id` value `20` as `Number`.
  See below screenshots:
  
  now select `PciRoot(0)/Pci(0x02,0)` now add `device-id` value `16190000' as 'Data`
  See below screenshots:
  
 now go to Clover Configurator->Graphics and make a sure Inject ATI, Inject Intel and  Inject NVidia is unchecked. See below screenshots:
 
 
