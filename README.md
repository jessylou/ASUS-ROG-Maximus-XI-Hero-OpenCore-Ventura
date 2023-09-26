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

| Model              | ASUS ROG Maximus XI Hero Hackintosh        |
|:-------------------|:-------------------------------------------|
| Processor          | Intel Core i5-6300U @ 2.40GHz 3MB L3 cache |
| Processor Family   | Skylake - 6th generetion - 14 nm - Q3'15   |
| Graphics           | Integrated Intel HD Graphics 520 32 MB     |
| Memory             | 16GB 2133MHz DDR4 SDRAM (Dual channel)     |
| Display            | 14" FHD (1920x1000) - Non-Touch LCD        |
| Storage            | 512GB M.2 SATA SSD                         |
| Audio              | RealTek ALC3235 24-bits                    |
| WLAN + Bluetooth   | Intel® Tri-Band Wireless-AC 18260 + BT 4.0 |
| LAN                | Ethernet 10/100/1000 Mb/s (RJ-45)          |
| Camera             | 1280x720 FHD Webcam                        |
| Fingerprint Reader | Yes                                        |
| USB 3.0            | USB 3.0 x 2 ports, 1 PowerShare port       |
| SD Card            | SD 4.0                                     |
| Smart Card         | Yes                                        |
| Keyboard           | Backlit Keyboard                           |
| Trackpad           | ALPS Touchpad                              |

To get more:

- [Dell Latitude E7470](https://www.dell.com/support/manuals/fr-fr/latitude-e7470-ultrabook/late_e7470_om/caract%C3%A9ristiques?guid=guid-5a37743b-091b-4716-9574-f99f29e7bf1c&lang=en-us)
- [Intel® Processor & Graphics](https://ark.intel.com/content/www/us/en/ark/products/88190/intel-core-i56300u-processor-3m-cache-up-to-3-00-ghz.html)
- [Intel® Wierless](https://www.intel.com/content/www/us/en/products/sku/88822/intel-triband-wirelessac-18260/specifications.html)
</details>

## Status

<details>
<summary><strong>What's working</strong></summary>
</br>

- [x] Intel HD 520 Graphics `incuding graphics acceleration`.
- [x] All USB ports.
- [x] Internal camera.
- [x] WiFi using [AirportItlwm](https://github.com/OpenIntelWireless/itlwm).
- [x] Bluetooth using [IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) (without IntelBluetoothInjector.kext), with BlueToolFixup.kext from: [BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM) and BlueToothFixup.kext from the same source.
- [x] Shutdown/ Reboot/ Sleep/ Wake.
- [x] Speakers and headphones jack.
- [x] Intel Gigabit Ethernet.
- [x] iMessage, FaceTime, App Store.
- [x] miniDP and HDMI with digital audio passthrough (if you experience cursor lags, try turning on and off one of the displays).
- [x] Keyboard and Trackpad(two finger vertical swipes).
- [x] DRM (Works with Google Chrome. Tested with Prime Video and Netflix).
- [x] Multitouch gestures for ALPS touchpad.
- [x] SD Card Reader using [RealtekCardReader.kext](https://github.com/0xFireWolf/RealtekCardReader) with [RealtekCardReaderFriend.kext](https://github.com/0xFireWolf/RealtekCardReaderFriend).

</details>

<details>
<summary><strong>What's not working</strong></summary>
</br>

- [ ] AirDrop

</details>

## Current configuration

Up to date on September 26th, 2023.
- macOS: Ventura 13.6
- OpenCore: 0.9.4

## Installation

