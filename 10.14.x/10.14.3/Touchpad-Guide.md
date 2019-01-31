
#  Installation

### Add the following kexts
- [VoodooPS2Controller.kext](https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller)

If you don't have this, no keyboard and no trackpad. We'll change it later to VoodooI2C, but for now you'll need to use this (works kinda jerky on trackpad) or connect external Keyboard/mouse

### Tools Used
- [Clover Configurator](http://mackie100projects.altervista.org/download-clover-configurator/)
- [iasl](https://bitbucket.org/RehabMan/acpica/downloads)
- [MaciASL](https://bitbucket.org/RehabMan/os-x-maciasl-patchmatic/downloads)

VoodooPS2Controller.kext
https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller
If you don't have this, no keyboard and no trackpad. We'll change it later to VoodooI2C, but for now you'll need to use this (works kinda jerky on trackpad) or connect external Keyboard/mouse

### ACPI Patch Step
- Reboot the laptop. At Clover boot screen press F4. This will dump files in EFI/Clover/ACPI/origin.
- Boot into macOS
- Mount your EFI drive in Clover Configurator
- Copy DSDT.aml and all SSDT*.aml from EFI/Clover/ACPI/origin to a new folder named DSDT on your desktop.
- Copy MaciASL from your USB flash drive to Applications

The guide talks about duplicate SSDTs and comparing their size. I have two SSDTs with the same size but not the same content so there will be no problems later on.

In Terminal:
Code:
```sh 
git clone https://github.com/RehabMan/Intel-iasl.git iasl.git
```

It should ask you to install git. Install git. Yes, you must do it again in case if you don't had command line tools
```sh
git clone https://github.com/RehabMan/Intel-iasl.git iasl.git
cd iasl.git
make
sudo make install
sudo cp /usr/bin/iasl /Applications/MaciASL.app/Contents/MacOS/iasl61
cd *drag and drop your DSDT folder*
```

This will put you back to DSDT folder
Code:
```sh
Code: iasl -da -dl *.aml
```

Open MaciASL
In preferences, sources tab

Add RehabMan's Laptop Patches
Site : http://raw.github.com/RehabMan/Laptop-DSDT-Patch/master

Add VoodooI2C patch repo (needed for touchpad)
https://github.com/alexandred/VoodooI2C-Patches

Open all of your dsl files from your DSDT folder.
You should have pretty much the same files as me if you have the same laptop.

For DSDT.dsl, wait for the file to load completely
Apply Brightness fix patch
Apply VoodooI2C GPIO Patch and Windows 10 Patch

Compile and if no errors, save the file as AML file (replace if needed).
Copy ONLY EDITED (don't copy if you didn't replace anything) files from DSDT folder to EFI/CLOVER/ACPI/patched

