
# Changelog

  - Updated OS (10.15.3 TO 10.15.4)
  - Modular patched DSDT(Removed SSDT-I320.aml added SSDT-EC-USBX.aml, SSDT-EC, SSDT-GPRW, SSDT-I2C etc).
  - Removed FakeSMC.kext(with sensors), ACPIBatteryManager.kext replaced with VirtualSMC.kext.
  - Removed USBInjectAll.kext added USBPorts.kext using Hackintool.
  - Updated clover and folder structure for UEF drivers.
  - Power management (Idle frequency is 0.4 GHz)