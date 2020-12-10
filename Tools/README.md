
# Tools

### extract_efi_without_serial.sh

Use script to extract your OpenCore folder without `SystemSerialNumber`, `SystemUUID` and `MLB`.

Uses:
First get the name of your EFI partition.

```
diskutil list
```

Go to `extract_efi_without_serial.sh` directory.
`First Argument($1)` =  `Device path` = `/dev/disk0s1`
`Second Argument($2)` = `Device name + OC Folder path` = `/Volumes/ESP/EFI/OC`

```
./extract_efi_without_serial.sh /dev/disk0s1  /Volumes/ESP/EFI/OC
```

This will output the zip of the OpenCore folder.
```
OC_OpenCoreVersion_ReleaseDate.zip
```

Example:
```
OC_063_2020_11_02.zip
```
