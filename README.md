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
| WLAN               |                                              |
| Bluetooth          | Intel® Tri-Band Wireless-AC 18260 + BT 4.0   |
| LAN                | Ethernet 10/100/1000 Mb/s (RJ-45)            |
| Camera             | Logitech Webcam C920 HD Pro                  |
| USB 3.1            | USB 3.0 x 2 ports, 1 PowerShare port         |
| Keyboard           | Backlit Keyboard                             |

To get more:

- [ASUS ROG Maximus XI Hero](https://rog.asus.com/motherboards/rog-maximus/rog-maximus-ix-hero-model/)
- [Intel® Processor](https://ark.intel.com/content/www/us/en/ark/products/190887/intel-core-i99900kf-processor-16m-cache-up-to-5-00-ghz.html)
- [IAMD Graphics](https://www.xfxforce.com/gpus/xfx-amd-radeon-tm-rx-580-gts-xxx-edition-8gb)

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

