# ASUS ROG Maximus XI Hero OpenCore & Ventura

<a ref="https://github.com/acidanthera/OpenCorePkg"><img src="https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png" width="200" height="48"><a/>

## Introduction

<details>
<summary><strong>Getting started</strong></summary>
</br>

**Meet the bootloader:**

- [Why OpenCore?](https://dortania.github.io/OpenCore-Install-Guide/why-oc.html)
- [Dortania's website](https://dortania.github.io)

**Recommended tools:**

- Plist editor: [ProperTree](https://github.com/corpnewt/ProperTree)
- EFI Partition Mounting Script: [MountEFI](https://github.com/corpnewt/MountEFI)

</details>

<details>
<summary><strong>My Hardware</strong></summary>
<br>
  
This ASUS Mother Board has been build in 2019.

| Model              | ASUS Hackintosh                              |
|:-------------------|:---------------------------------------------|
| Motherboard        | ASUS ROG Maximus XI Hero (Z390, LGA1151)     |
| Processor          | Intel Core i9-9900KF @ 3.6GHz 16MB cache     |
| Processor Family   | Coffee Lake - 9th generetion - 14 nm - Q1'19 |
| Graphics           | XFX Radeon RX 580 (AMD) - 8GB                |
| Memory             | 64GB 3200MHz DDR4                            |
| Cooler             | H60 Corsair Liquid Cooler                    |
| Storage HD         | Seagate Barracuda 2 TB                       |
| Storage SSD        | SSD Samsung EVO 860 500 MB                   |
| Storage NVMe       | Western Digital Black SN850X 1 TB            |
| Mouse              | Apple Magic Mouse 2                          |
| Audio              | RealTek ALC3235 24-bits                      |
| WiFi               | TP-Link model Archer T9E AC1900 802.11ac     |
| Bluetooth          | IOGear GBU 521 W6 BT 4.0 USB (BCM20702A0)    |
| LAN                | Ethernet 10/100/1000 Mb/s (RJ-45)            |
| Camera             | Logitech Webcam C920 HD Pro                  |
| USB 3.1            | USB 3.1 x 4 ports, 1 PowerShare port         |
| Keyboard           | Logitech MX Keys with backlit                |

To get more:

- [ASUS ROG Maximus XI Hero](https://rog.asus.com/motherboards/rog-maximus/rog-maximus-ix-hero-model/)
- [Intel® Processor](https://ark.intel.com/content/www/us/en/ark/products/190887/intel-core-i99900kf-processor-16m-cache-up-to-5-00-ghz.html)
- [AMD Graphics](https://www.xfxforce.com/gpus/xfx-amd-radeon-tm-rx-580-gts-xxx-edition-8gb)
- [TP-Link WiFi](https://www.tp-link.com/en/home-networking/pci-adapter/archer-t9e/#specifications)

As the WiFi card is based on BCM4360 chipset, there is no need to add any kext: Ventura is running perfectly by default.

</details>

## Status

<details>
<summary><strong>What's working</strong></summary>
</br>

- [x] Graphics `incuding graphics acceleration`.
- [x] All USB ports.
- [x] Camera.
- [x] WiFi.
- [x] Bluetooth.
- [x] Shutdown/ Reboot/ Sleep/ Wake.
- [x] Speakers and headphones jack.
- [x] Gigabit Ethernet.
- [x] iMessage, FaceTime, App Store.
- [x] Keyboard.

</details>

<details>
<summary><strong>What's not working</strong></summary>
</br>

- [ ] AirDrop

</details>

## Current configuration

Change on November 12th, 2023:
- macOS: Ventura 13.6.1
- OpenCore: 0.9.6

## Installation

<details>
<summary><strong>Create the USB</strong></summary>
</br>

Follow the [guide on the OpenCore documentation](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) to create a USB for installation. Choose the operating system you use to create the USB and proceed with the guide. At the end of the Create USB section, OpenCore will ask us to do additional configurations. We don't need to do any of that because the `EFI` folder in this repository provides all necessary configurations we need for installation on Dell Latitude E7470.
</details>

<details>
<summary><strong>Boot and Install macOS</strong></summary>
</br>

- Plug in the USB we created to your Dell computer
- Press the Power button to turn on our computer (if you used the Dell to create the USB, shutdown the computer first)
- Wait and we will see the Apple icon on a black screen with a progress bar at the bottom
- Then, we will see a menu with four options. Make sure select `Disk Utility` to partition your disk appropriately and format the partition for installing macOS into `APFS`. If you are dual booting with other operating systems, an easier way would be to partition the drive beforehand as some formats like NTFS are readonly on macOS.
- Follow the installation steps and configure the preferences to your liking
- Log in to macOS and enjoy

</details>

## Post Installation

<details>
<summary><strong>Booting without USB</strong></summary>
</br>

You need to plug in the installation USB created previously everytime you start macOS after shutdown. If you want to boot without the USB, follow [this guide by OpenCore](https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html#grabbing-opencore-off-the-usb).

</details>

<details>
<summary><strong>Update Instructions</strong></summary>
</br>

- To update from an older version of EFI to the current one, download this repository and replace your EFI folder with this one. Make sure you use your own SMBIOS, the included one is only for reference.

- After update, you can check your current OpenCore version by typing the following line in the Terminal:
```
nvram 4D1FDA02-38C7-4A6A-9CC6-4BCCA8B30102:opencore-version
```
You may see a line printed as follows:
```
4D1FDA02-38C7-4A6A-9CC6-4BCCA8B30102:opencore-version   REL-093-2023-06-12
```
where `REL` means a RELEASE version of OC, `093` means version 0.7.4, and `2023-06-12` is the date of the release.

</details>

<details>
<summary><strong>Fixing iServices</strong></summary>
</br>

- In order to get Apple Services like App Store working, you need to generate your own SMBIOS(The included one is only for reference).

- For more information on how to do that, visit the [Dortania Guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial).

</details>

## Credits

- [Acidanthera](https://github.com/acidanthera) for OpenCore, Lilu and related kexts.
- [Dortania](https://dortania.github.io) for installation and other guides.
- Everyone else who contributed to this repository directly/indirectly.
