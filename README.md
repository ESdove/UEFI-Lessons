These series of lessons are intendend to get you started with UEFI programming in Linux with the help of [EDKII](https://github.com/tianocore/edk2).

# Content

- [Lesson 00](Lessons/Lesson_00): Getting started guide for EDKII. Compile OVMF and run it in QEMU
- [Lesson 01](Lessons/Lesson_01): Create a simplest app and run it in OVMF
- [Lesson 02](Lessons/Lesson_02): Create a simplest package
- [Lesson 03](Lessons/Lesson_03): Create `HelloWorld` app with the help of SystemTable services
- [Lesson 04](Lessons/Lesson_04): Use edk2 libraries to simplify our `HelloWorld` app
- [Lesson 05](Lessons/Lesson_05): Simplify build command with the help of files in the `Conf` folder
- [Lesson 06](Lessons/Lesson_06): Handle/Protocol databases internals - Part 1: Theory and raw access to an app ImageHandle
- [Lesson 07](Lessons/Lesson_07): Handle/Protocol databases internals - Part 2: Raw access to app protocols
- [Lesson 08](Lessons/Lesson_08): `HandleProtocol` API function. Information from the `ImageHandle` protocols
- [Lesson 09](Lessons/Lesson_09): Get ImageHandle protocols with the `ProtocolsPerHandle` API function
- [Lesson 10](Lessons/Lesson_10): `EFI_STATUS` type and `EFI_ERROR` macros
- [Lesson 11](Lessons/Lesson_11): Get EFI memory map information
- [Lesson 12](Lessons/Lesson_12): `EFI_SHELL_PARAMETERS_PROTOCOL`. Transform our EFI memory map to the Linux kernel style
- [Lesson 13](Lessons/Lesson_13): `ShellAppMain` entry point
- [Lesson 14](Lessons/Lesson_14): Get all variable names and GUIDs with the `gRT->GetNextVariableName` API
- [Lesson 15](Lessons/Lesson_15): Get and parse boot variables (BootOrder/BootCurrent/BootXXXX) with the `gRT->GetVariable` API
- [Lesson 16](Lessons/Lesson_16): Build our own boot option inside OVMF image similar to the UEFI shell app
- [Lesson 17](Lessons/Lesson_17): Add `WaitForEvent` function to our boot option app to see its output on booting
- [Lesson 18](Lessons/Lesson_18): Handle input from user with the `ReadKeyStroke` function
- [Lesson 19](Lessons/Lesson_19): Boot option modification with the help of `bcfg` command
- [Lesson 20](Lessons/Lesson_20): Intro to Platfrom Configuration Database (PCD). Declare and get simple fixed PCD
- [Lesson 21](Lessons/Lesson_21): Override order for PCD variables
- [Lesson 22](Lessons/Lesson_22): Feature flag PCD and its comparision to BOOLEAN fixed at build PCD
- [Lesson 23](Lessons/Lesson_23): PatchableInModule PCDs and how they can be changed via `GenPatchPcdTable`/`PatchPcdValue` utilities 
- [Lesson 24](Lessons/Lesson_24): Dynamic/DynamicEx PCDs
- [Lesson 25](Lessons/Lesson_25): More on PCDs
- [Lesson 26](Lessons/Lesson_26): Tables referenced in `EFI_CONFIGURATION_TABLE`
- [Lesson 27](Lessons/Lesson_27): Get SMBIOS information with `dmem`/`EFI_SMBIOS_PROTOCOL`/`smbiosview`
- [Lesson 28](Lessons/Lesson_28): Get ACPI tables and save them to files with a help of `EFI_SHELL_PROTOCOL`
- [Lesson 29](Lessons/Lesson_29): Use `EFI_ACPI_SDT_PROTOCOL` and `ShellLib` to save a BMP image from the ACPI BGRT table
- [Lesson 30](Lessons/Lesson_30): Find all PCI root bridges in the system with a help of `LocateHandleBuffer`/`OpenProtocol` functions and use
`EFI_PCI_ROOT_BRIDGE_IO_PROTOCOL` to get all PCI functions in the system.
- [Lesson 31](Lessons/Lesson_31): Search `pci.ids` database to get PCI Vendor/Device information with a help of `ShellLib`/`PrintLib` functions
- [Lesson 32](Lessons/Lesson_32): Show PCI Option ROM images with the help of `EFI_PCI_IO_PROTOCOL` protocol
- [Lesson 33](Lessons/Lesson_33): Use `EfiRom` utility for parsing and creation of PCI Option ROM images 
- [Lesson 34](Lessons/Lesson_34): Create a simple UEFI driver. Use `load`/`unload` UEFI shell commands to work with a driver image 
- [Lesson 35](Lessons/Lesson_35): Create a simple library and use it in an app
- [Lesson 36](Lessons/Lesson_36): Library constructor and destructor. `NULL` libraries
- [Lesson 37](Lessons/Lesson_37): Investigate ways how to add `acpiview` command functionality to your shell
- [Lesson 38](Lessons/Lesson_38): Create and use your custom protocol. `InstallMultipleProtocolInterfaces` and `UninstallMultipleProtocolInterfaces` functions
- [Lesson 39](Lessons/Lesson_39): Create a driver that adds hot key functionality with a help of `RegisterKeyNotify`/`UnregisterKeyNotify` functions
- [Lesson 40](Lessons/Lesson_40): `Key####` NVRAM variables
- [Lesson 41](Lessons/Lesson_41): `DEBUG` print statement internals. `EFI_D_*` log levels and all the PCDs for the `DEBUG` statement control. Getting and parsing OVMF boot log.
- [Lesson 42](Lessons/Lesson_42): Debug your drivers/applications and OVMF itself with GDB
- [Lesson 43](Lessons/Lesson_43): Intro to the HII. Create an application to display HII database content 
- [Lesson 44](Lessons/Lesson_44): HII database internals 
- [Lesson 45](Lessons/Lesson_45): Use `NewPackageList` from the `EFI_HII_DATABASE_PROTOCOL` directly to publish HII Package list with Strings packages. Part 1: Investigate common aspects of Package List data generation 
- [Lesson 46](Lessons/Lesson_46): Use `NewPackageList` from the `EFI_HII_DATABASE_PROTOCOL` directly to publish HII Package list with Strings packages. Part 2: String Packages data generation
- [Lesson 47](Lessons/Lesson_47): Use `NewPackageList` from the `EFI_HII_DATABASE_PROTOCOL` directly to publish HII Package list with Strings packages. Part 3: Combine everything together. Use `NewPackageList` and `GetString` protocol functions
- [Lesson 48](Lessons/Lesson_48): Use `UNI` files and `HiiLib` to publish and work with HII String packages
- [Lesson 49](Lessons/Lesson_49): UNI files declared with the help of `MODULE_UNI_FILE`/`PACKAGE_UNI_FILE`/`[UserExtensions.TianoCore."ExtraFiles"]`
- [Lesson 50](Lessons/Lesson_50): Use `UEFI_HII_RESOURCE_SECTION` to publish HII Package list with Strings packages
- [Lesson 51](Lessons/Lesson_51): Add manual to UEFI application. How `-?` and `help` work in shell. `EFI_SHELL_GET_HELP_TEXT` function from the `EFI_SHELL_PROTOCOL`
- [Lesson 52](Lessons/Lesson_52): Add Russian font - Part 1: investigate `EFI_NARROW_GLYPH`/`EFI_WIDE_GLYPH` format, construct glyph array from the *.woff font file
- [Lesson 53](Lessons/Lesson_53): Add Russian font - Part 2: construct `EFI_HII_SIMPLE_FONT_PACKAGE` and populate it to the HII database 
- [Lesson 54](Lessons/Lesson_54): Use `NewString` and `SetString` functions from the `EFI_HII_STRING_PROTOCOL` to add String Package for another language dynamically 
- [Lesson 55](Lessons/Lesson_55): Try to modify `PlatformLangCodes` EFI variable and add another language dynamically. Variable protection with a help of `EDKII_VARIABLE_POLICY_PROTOCOL`
- [Lesson 56](Lessons/Lesson_56): How to get module `FILE_GUID` and `BASE_NAME` in code. Autoconf variables `gEfiCallerIdGuid`/`gEdkiiDscPlatformGuid`/`gEfiCallerBaseName` 
- [Lesson 57](Lessons/Lesson_57): Use VFR to create a simple form and display it with a help of `EFI_FORM_BROWSER2_PROTOCOL.SendForm()`. IFR data investigation
- [Lesson 58](Lessons/Lesson_58): `subtitle` and `text` VFR elements
- [Lesson 59](Lessons/Lesson_59): Create an application to display HII Forms by package list GUIDs. Convert our simple form application to UEFI driver form
- [Lesson 60](Lessons/Lesson_60): Use `gRT->SetVariable()` function to create and delete UEFI variables. Investigate variable attributes. Practical uses of the `dmpstore` command
- [Lesson 61](Lessons/Lesson_61): Use `dmpstore` command to save/load variables to/from files. Write an application to recalculate CRC32 checksums in the `dmpstore` variable dumps
- [Lesson 62](Lessons/Lesson_62): Structure of the UEFI `Device path`. Dynamic and static Device paths. Interation over Device paths
- [Lesson 63](Lessons/Lesson_63): Create HII Form with a checkbox - Part 1: VFR code for `checkbox` element and `efivarstore` element
- [Lesson 64](Lessons/Lesson_64): Create HII Form with a checkbox - Part 2: Necessary code for `efivarstore` to work correctly


_____

# Learning links

1) Beyond BIOS: Developing with the Unified Extensible Firmware Interface, Third Edition by Vincent Zimmer and Michael Rothman (https://www.amazon.com/Beyond-BIOS-Developing-Extensible-Interface/dp/1501514784)

2) Harnessing the Uefi Shell: Moving The Platform Beyond Dos, Second Edition by Michael Rothman and Vincent Zimmer (https://www.amazon.com/Harnessing-UEFI-Shell-Moving-Platform/dp/1501514806)

3) https://github.com/tianocore-training

https://github.com/Laurie0131

4) https://blog.fpmurphy.com/

https://github.com/fpmurphy/UEFI-Utilities-2019

5) https://github.com/andreiw/UefiToolsPkg

_______

Check these if you don't afraid of the Chinese language:

6) Principles and Programming of UEFI, Dai Zhenghua
(https://www.amazon.com/Combat-UEFI-Principles-Programming-Chinese/dp/B07W3GFLRM)

https://github.com/zhenghuadai/uefi-programming

7) http://www.lab-z.com/iof/

8) https://blog.csdn.net/luobing4365

https://gitee.com/luobing4365/uefi-explorer

_______

And for the Russian speakers:

9) https://habr.com/ru/users/CodeRush/posts/

# Specifications

UEFI specifications (https://uefi.org/specifications):
- [UEFI Specification](https://uefi.org/sites/default/files/resources/UEFI_Spec_2_9_2021_03_18.pdf)
- [UEFI Platform Initialization Specification](https://uefi.org/sites/default/files/resources/PI_Spec_1_7_A_final_May1.pdf)
- [UEFI Shell Specification](http://www.uefi.org/sites/default/files/resources/UEFI_Shell_2_2.pdf)

EDK2 specifications (https://github.com/tianocore/tianocore.github.io/wiki/EDK-II-Documentation#specifications):
- [Build Specification](https://edk2-docs.gitbook.io/edk-ii-build-specification/)
- [Platform Description (DSC) File Specification](https://edk2-docs.gitbook.io/edk-ii-dsc-specification/)
- [Package Declaration (DEC) File Format Specification](https://edk2-docs.gitbook.io/edk-ii-dec-specification/)
- [Module Information (INF) File Specification](https://edk2-docs.gitbook.io/edk-ii-inf-specification/)
- [Flash Description (FDF) File Specification](https://edk2-docs.gitbook.io/edk-ii-fdf-specification/)
- [Platform Configuration Database Infrastructure Description](https://edk2-docs.gitbook.io/edk-ii-pcd-specification/)
- [Multi-String .UNI File Format Specification](https://edk2-docs.gitbook.io/edk-ii-uni-specification/)
- [VFR Programming Language Specification](https://edk2-docs.gitbook.io/edk-ii-vfr-specification/)
- [Driver Writer's Guide](https://edk2-docs.gitbook.io/edk-ii-uefi-driver-writer-s-guide/)
- [Module Writer's Guide](https://edk2-docs.gitbook.io/edk-ii-module-writer-s-guide/)
- [EDKII User Manual](https://github.com/tianocore-docs/Docs/raw/master/User_Docs/EDK_II_UserManual_0_7.pdf)

# Tools

- [UEFITool](https://github.com/LongSoft/UEFITool) - UEFITool is a cross-platform C++/Qt program for parsing, extracting and modifying UEFI firmware images
- [CrScreenshotDxe](https://github.com/LongSoft/CrScreenshotDxe) - UEFI DXE driver to take screenshots from GOP-compatible graphic consoles
- [RU.EFI](http://ruexe.blogspot.com/) - "Read Universal" - UEFI application to debug UEFI interfaces
