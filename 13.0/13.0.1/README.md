
### Changelog
 1. macOS Ventura 13.0.1 support added.
 2. OpenCore version updated to 0.8.6.
 3. Removed `BrcmFirmwareData.kext`, `BrcmPatchRAM3.kext`, `IntelBluetoothInjector.kext`, `itlwm.kext`, `VoodooTSCSync.kext`, `YogaSMC.kext`, `YogaSMCAlter.kext` - not needed.
 4. Added `IntelBTPatcher.kext`, `RestrictEvents.kext`
 5. Removed `SSDT-ARTC.aml`, `SSDT-DDGPU.aml`, `SSDT-EC.aml`, `SSDT-ECRW.aml`, `SSDT-LPC.aml`, `SSDT-PrtSc-F13.dsl`, `SSDT-Q10Q11.aml`, `SSDT-RCSM.aml`, `SSDT-SATA.aml`, `SSDT-SMBUS.aml`.
 6. Inject Kaby Lake graphics.  


### What's Working/Not working
 1. Need to check why `HEVC` encoding not working on `IdeaPad 320 15ISK`
 2. Color banding and graphics issues 


### Important
Please add `SystemSerialNumber`, `SystemUUID` and `MLB`.
Please backup your efi before upgrading.
For macOS 12.0 lower please inject HD520 graphics.


### Download
Please check release section to download.
