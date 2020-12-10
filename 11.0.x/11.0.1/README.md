
### Changelog
 1. macOS Big Sur 11.0.1 support added.
 2. OpenCore version updated to 0.6.4.
 3. Removed `framebuffer-unifiedmem` . If you are running `4k` you can uncomment this property. see `
 4. Removed `AAPL, slot-name` because of `HEVC is not working on bigSur but working on Catalina` Thanks to user [btx3](https://github.com/btx3) for reporting issue [#39](https://github.com/gajjartejas/Lenovo-Ideapad-320-15ISK-14ISK-Laptop-Hackintosh/issues/39).
 5. Added `YogaSMC` Please see https://github.com/zhen-zen/YogaSMC
    1. Supports `Conservation mode`  and `Fn lock mode`
    2. Note: You have to manually enable driver from `Kernal` -> `YogaSMCAlter.kext` and enable it. Download and install `YogaSMCNC.app` and `YogaSMCPane.prefPane`.
 6. Kexts updated.


### What's Working/Not working
 1. Micro SD Card Reader - Not working in OpenCore.
 2. Need to check why `HEVC` encoding not working on `IdeaPad 320 15ISK`


### Important
Please add `SystemSerialNumber`, `SystemUUID` and `MLB`.


### Download
Please check release section to download.
