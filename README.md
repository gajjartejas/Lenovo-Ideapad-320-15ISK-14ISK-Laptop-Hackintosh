 
 [<img align="right" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/instagram.svg" width="50" height="50" />](http://www.instagram.com/gajjartejas)
 [<img align="right" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/twitter.svg" width="50" height="50" />](http://www.twitter.com/gajjartejas)
 [<img align="right" src="https://cdn.jsdelivr.net/npm/simple-icons@latest/icons/reddit.svg" width="50" height="50" />](http://www.reddit.com/u/gajjartejas)

# Lenovo-Ideapad-320-15ISK-14ISK-Laptop-Hackintosh
Goal of this repo is to run Mac os on Lenovo Ideapad 320 15ISK Laptop

macOS Mojave 10.14.6            |  macOS Catalina 10.15.6
:-------------------------:|:-------------------------:
![alt text](10.14.x/10.14.6/Screenshot.png)  |  ![alt text](10.15.x/10.15.6/screenshot.png)

## macOS Mojave to Catalina direct upgrade note:
 Download latest [Clover](10.15.x/10.15.4/CLOVER.zip) and overwrite with existing one and update all kexts to latest version

## Detailed Installation Guide

Go to [INSTALLATION_GUIDE_BEGINNERS.md](INSTALLATION_GUIDE_BEGINNERS.md)(**For beginners**)

Go to [INSTALLATION_GUIDE.md](INSTALLATION_GUIDE.md)(**Detailed guide - Advanced user only**)

Go to [WIRELESS_CARD_BUYING_GUIDE.md](WIRELESS_CARD_BUYING_GUIDE.md)(**Supported WiFi adapters and buying guide**)

## About this Laptop

## Hardware Info 💻

Type | Spec | Status | Link
---------|:---------:|----------:|----------
Computer		| Lenovo Ideapad 320-15ISK 80XH01DNIN   | Working | -
BIOS Version	| LENOVO Insyde EFI(4WCN29WW) | Working | -
CPU				| DualCore Intel Core i3, 2000 MHz (20 x 100) | Working | -
Chipset			| Intel Sunrise Point-LP, Intel Skylake-U | Working | -
Graphics		| Intel HD Graphics 520, NVIDIA GeForce 920MX (Using Intel GPU only) | Working | [Guide](https://www.tonymacx86.com/threads/guide-intel-framebuffer-patching-using-whatevergreen.256490/)
Audio			| Realtek ALC3240, Codec ID:10EC0230h / 17AA3809h | Working | [Guide](https://github.com/acidanthera/AppleALC/wiki/Installation-and-usage)
Ethernet		| Realtek RTL8168/8111 PCI-E Gigabit Ethernet Adapter() | Working | -
WiFi			| Intel(R) Dual Band Wireless-AC 3165 | Not Working | -
Bluetooth		| Intel(R) Wireless Bluetooth(R) | Working | -
Touchpad		| I2C ELAN0608 | Working | [Guide](Touchpad-Guide.md)
Keyboard		| - | Working | -
Webcam		| Ven id: 0x04f2(Chicony Electronics Co.,Ltd.) Product id: 0xb5d8| Working | -
Battery		|   Serial Number: L16M2PB2- 1229 Manufacturer: SMP Device Name:	L16M2PB2 | Working | -

## Modifications 🔨

Type | Spec | Status
---------|:---------:|----------
D-Link DWA-131 Wireless N Nano USB Adapter (Black) 		| - | Working
BCM94360CS2 Wireless WIFI Bluetooth 4.0 Airport Card For Macbook Air 11" A1465 13" A1466 2013 MD711LL/A MD760 BCM94360CS2AX 		| - | Working
Wireless Bluetooth Mouse Rechargeable Mouse		| - | Working
Universal for 9.5mm CD/DVD Drive Slot (for SSD and HDD)		| - | Working
15.6 inch IPS LCD matrix LP156WF4 LP156WF6 | - | Working
## Software Status 👨‍💻

Type | Spec | Status
---------|:---------:|----------
Battery Status		| - | Working
Brightness With keys(F11 - F12)		| - | Working
Sleep/Hibernate		| - | Unknown

## Kext Used

Kext | Info 
---------|:---------
AppleALC.kext | For Audio
Lilu.kext | Arbitrary kext and process patching on macOS
RealtekRTL8111.kext | RTL8111/8168/8411 PCI Express Gigabit Ethernet
SMCBatteryManager.kext | Battery Status Monitoring
VirtualSMC.kext | SMC Emulator Layer
SMCProcessor.kext | Processor Temp Monitoring
SMCSuperIO.kext | Fan Reading
USBPorts.kext | For USB Prot
VoodooI2C.kext | For I2C Touchpad
VoodooI2CELAN.kext | For ELAN Touchpad
VoodooPS2Controller.kext | Contains updated Voodoo PS/2 Controller, improved Keyboard & Synaptics TouchPad
WhateverGreen.kext | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs

