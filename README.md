
<img align="left" height="150" src="https://github.com/user-attachments/assets/4bbeca09-c1fb-4f80-8a0c-38e8cc3dfb37">

<img align="left" src="https://github.com/Coopydood/ultimate-macOS-KVM/assets/39441479/8f69f9b9-cf23-4e8b-adf3-95862a23e2ba" height=210 width=1 />

<a href="https://coopydood.github.io/ultimate-macOS-KVM"></a><h3>OpenCore OptiPlex 7060 SFF (Coffee Lake)</h3>

OpenCore Hackintosh configuration example for the **Dell OptiPlex 7060 Small Form Factor** with an Intel® Core™ i7-8700. 
<br>

[![GitHub](https://img.shields.io/github/license/Coopydood/OpenCore-OptiPlex-7060?label=Licence&logo=unlicense&logoColor=white&style=for-the-badge)](https://github.com/Coopydood/OpenCore-OptiPlex-7060/blob/main/LICENSE) [![GitHub repo size](https://img.shields.io/github/repo-size/Coopydood/OpenCore-OptiPlex-7060?color=07b55b&label=Size&logo=envoy-proxy&logoColor=white&style=for-the-badge)](https://github.com/Coopydood/OpenCore-OptiPlex-7060) [![Discord](https://img.shields.io/discord/574943603466436628?color=7d86ff&label=Discord&logo=discord&logoColor=white&style=for-the-badge)](https://discord.gg/WzWkSsT)

<br><br>

***

<img src="https://github.com/user-attachments/assets/29dcd7a4-90cf-45b4-b23f-2bda1a87d223" alt="big man OptiPlex 7060 SFF" width="1400"/><br>
<p align="center"><i>This OptiPlex doesn't dream in Excel spreadsheets anymore.</i></p>


***

## OpenCore

<img align="left" width="100" height="100" src="https://dortania.github.io/docs/latest/Logos/Logo.png">
<img align="left" src="https://github.com/Coopydood/ultimate-macOS-KVM/assets/39441479/8f69f9b9-cf23-4e8b-adf3-95862a23e2ba" height=100 width=2 />
<h3>OpenCore<br><sub>1.0.1</sub></h3>

This is the version of OpenCore used, including bundled files. The included ``config.plist`` targets this version.
<br>


## macOS

<img align="left" width="90" height="90" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/aa49b5ba-6cca-4dab-bcfc-6bf21909e738">
<!-- CHANGE THE IMAGE URL TO THE MAIN OS YOUR CONFIG TARGETS. IMAGE URL LIST BELOW! -->

<img align="left" src="https://github.com/Coopydood/ultimate-macOS-KVM/assets/39441479/8f69f9b9-cf23-4e8b-adf3-95862a23e2ba" height=480 width=2 /> 
<!-- CHANGE THE HEIGHT WHEN ADDING OR REMOVING SUPPORTED OSES TO THE LIST (Default: 520) -->

<h3>macOS Sonoma<br></h3>

This is the version of macOS that this OpenCore configuration currently targets. Other versions of macOS that are compatible with it are listed below.<br>

#### Supported

<img align="left" width="35" height="35" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/4829ebb4-ce7f-4ecf-8309-d691c9361f6b"> 
<h5>macOS Ventura</h5>
<img align="left" width="35" height="35" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/7d341cce-4370-4430-b3d5-bf1868afe4a3"> 
<h5>macOS Monterey</h5>
<img align="left" width="35" height="35" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/79a7a051-0f5a-419e-8544-b51b1572d3b9"> 
<h5>macOS Big Sur</h5>
<img align="left" width="35" height="35" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/cd8029e8-c256-4295-9908-37809d64dcfe"> 
<h5>macOS Catalina</h5>
<img align="left" width="35" height="35" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/184bb2ef-c447-4cbd-b07c-8b4b096e3944"> 
<h5>macOS Mojave</h5>
<img align="left" width="35" height="35" src="https://github.com/Coopydood/OpenCore-Z490E-CometLake/assets/39441479/bd4a791d-1ac2-4a9a-8ee0-22e4d5f88cd3"> 
<h5>macOS High Sierra</h5>

<br><br><br>

***


## What works?

### macOS

- [x] macOS Sonoma

### Hardware

- [x] iGPU (Intel UHD Graphics 630)
- [x] dGPU (AMD Radeon RX 550)
- [x] SATA drive
- [x] USB 3.1 (XHCI)
- [x] Ethernet
- [ ] Wi-Fi
- [ ] Bluetooth
- [x] Sound
- [x] Hyperthreading  

### Software

- [ ] AirDrop
- [x] iMessage
- [x] FaceTime
- [ ] Unlock with Apple Watch
- [x] QE/CI graphics acceleration
- [x] Metal support
- [x] Temperature sensors
- [ ] Sleep / Wake
- [x] Virtualisation
- [x] Memory bank configuration
- [x] Boot chime

> [!IMPORTANT]
> This machine does NOT yet have a Wi-Fi / Bluetooth card. I plan on adding this in the future.

<br>

***

## Problems

<ul>
<li><b>Sleep / Wake</b></li>
Unfortunately, sleep is broken on this system at the moment. The system itself can go into and out of the sleep state, but the monitor never wakes up. My <a href="https://github.com/Coopydood/OpenCore-OptiPlex7050-Micro">other OptiPlex hacc</a> does this too. I'll investigate this!
  
<br><br>

<li><b><s>External Audio and HDMI Output</s> ‏‏‎ ‏‏‎ ‎‎‏‏‎ ‎ 🎉 FIXED!</b></li>
<s>Unfortunately, external audio - both DisplayPort and HDMI - doesn't work. HDMI output is also broken, with the system failing to boot with only HDMI plugged in. Strangely, once booted, the system does half-work with HDMI, but is locked at low resolution.</s>

> [!TIP]
> This was fixed by using a combo of DeviceProperties entries from <a href="https://github.com/AurelienAudero/Intel-i5-7400-Hackintosh-EFI">this excellent repo</a>!


</ul>


***

## System

The specs of the main system that the OpenCore configuration targets.

| **Motherboard** |                  Dell                 |
|-----------------|:-------------------------------------------------------------:|
| **CPU**         |                      Intel® Core™ i7-8700                     |
| **Chipset**     |                             OptiPlex 7060 SFF                            |
| **Generation**  |                           Coffee Lake                          |
| **Memory**      |                       16 GB DDR4                       |
| **Storage**     |                     500 GB SATA SSD                    |
| **GPU**         | Intel UHD Graphics 630<br>AMD Radeon RX 550 |
| **NIC**         |                  Intel I219-LM                  |

***

## ACPI

SSDTs used:
- SSDT-AWAC
- SSDT-EC-USBX-DESKTOP
- SSDT-HPET *
- SSDT-PLUG
- SSDT-PMC

> [!IMPORTANT]
> ``SSDT-HPET`` was compiled by me specifically for this machine model. Along with several ACPI patches, this is used to fix **onboard audio, including internal speakers.** Without it, macOS will show as having no built-in audio devices.  
  
***

## DeviceProperties

The following tables display the added PCI devices and their child keys.

### PciRoot(0x0)/Pci(0x1,0x0)/Pci(0x0,0x0)

AMD Radeon RX 550

| **Key**                  | **Type** |   **Value**  |
|--------------------------|:--------:|:------------:|
| device-id                |   Data   | ``FF67`` |
| model                    |   String | ``AMD Radeon RX 550`` |

> [!IMPORTANT]
> The Dell OEM variant of the RX 550 uses the **Lexa** core. This does NOT officially have support in macOS... *or does it*? Simply masking it as the Baffin core version works perfectly! Just make sure to add the mask, as seen here.

<br>

### PciRoot(0x0)/Pci(0x1F,0x3)

Internal Speakers

| **Key**                  | **Type** |   **Value**  |
|--------------------------|:--------:|:------------:|
| AAPL,slot-name           |   String | ``Internal`` |
| device_type              |   String | ``Audio device`` |
| layout-id                |   Data   | ``0B000000`` |

<br>

### PciRoot(0x0)/Pci(0x2,0x0)

Intel UHD Graphics 630

| **Key**                  	| **Type** 	| **Value**                 	|
|--------------------------	|:----------:|:---------------------------:|
| AAPL,ig-platform-id      	|   Data   	|        ``0000923E``       	|
| device-id                	|   Data   	|        ``9B3E0000``       	|
| framebuffer-patch-enable 	|   Data   	|        ``01000000``       	|
| framebuffer-stolenmem    	|   Data   	|        ``00003001``       	|
| enable-metal             	|   Data   	|        ``01000000``       	|

<br>


***

## Kernel

The following shows the kernel configuration.

### Kexts

Kexts used:
- Lilu
- WhateverGreen
- AppleALC
- IntelMausi
- RestrictEvents
- RTCMemoryFixup
- SMCProcessor
- SMCSuperIO
- SMCDellSensors
- VirtualSMC
- OptiPlex7060_SFF_USBMap *
- ~~USBMapDummy~~

> [!IMPORTANT]
> The ``OptiPlex7060_SFF_USBMap.kext`` is the USB map created manually by me on my own system. It may or may not work for other 7060 SFF machines. If it doesn't work, please disable it.

> [!TIP]
> In case you need it for your own mapping, ``USBMapDummy.kext`` has been left included but disabled, so you can enable it if you need it.


### Patches

None

***

## Security

**SecureBootModel 》** ``x86legacy``

**Vault 》** Optional


***

## NVRAM

Contents stored in NVRAM.

<br>

### 4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14

| **Key**                | **Type** |   **Value**  |
|------------------------|:--------:|:------------:|
| DefaultBackgroundColor |   Data   | ``00000000`` |

<br>

### 4D1FDA02-38C7-4A6A-9CC6-4BCCA8B30102

| **Key**       | **Type** | **Value** |
|---------------|:--------:|:---------:|
| rtc-blacklist |   Data   |           |

<br>

### 7C436110-AB2A-4BBB-A880-FE41995C9F82

| **Key**                   | **Type** |                                    **Value**                                   |
|---------------------------|:--------:|:------------------------------------------------------------------------------:|
| ForceDisplayRotationInEFI |  Number  |                                        0                                       |
| SystemAudioVolume         |   Data   |                                     ``46``                                     |
| boot-args                 |  String  | keepsyms=1 debug=0x100 alcid=11 -cdfon -igfxmpc -igfxcdc igfxrpsc=1 revpatch=sbvmm |
| csr-active-config         |   Data   |                                  ``00000000``                                  |
| prev-lang-diags:kbd       |   Data   |                                 ``656E2D47 42``                                |
| prev-lang:kbd             |   Data   |                               ``656E2D47 423A32``                              |                                      |
| StartupMute               |   Data   |                                     ``00``                                     |

***

## SMBIOS

### iMac19,2

This model of iMac has a direct hit on the CPU model used on this machine (i7-8700). As a result, it's the most appropriate SMBIOS. However, it may have to be changed soon if Apple drops support (or we pray to OCLP).

***

## UEFI

Drivers in use:

- HFSPlus
- OpenRuntime
- OpenCanopy
- AudioDxe *

>[!NOTE]
``AudioDxe`` is loaded so that OpenCore can make a boot chime on startup!
  
***

## Post-Install Tweaks

This is just a collection of my post-install tweaks I apply after installing macOS. They're not really related to OpenCore or the overall functionality of the configuration.

<details><summary><h4>Dark Menu Bar and Dock</h4></summary>

Okay, so I'm a bit of a macOS boomer. Having used macOS since long before Mojave's *dark mode*, I'm accustomed to the regular light appearance of the windows - but I always enabled the "Dark menu bar and dock" option as I loved the look. While I still like dark mode (and use it on iOS), the hybrid light/dark mode on macOS is still my favourite!

The following commands restore that functionality:

**Window Server**
```sh
defaults write -g NSRequiresAquaSystemAppearance -bool Yes
```

**Notification Centre**
```sh
defaults write com.apple.notificationcenterui NSRequiresAquaSystemAppearance -bool No
```

**Control Centre**
```sh
defaults write com.apple.controlcenterui NSRequiresAquaSystemAppearance -bool No
```

**About This Mac + System Profiler**
```sh
defaults write com.apple.SystemProfiler.AboutExtension NSRequiresAquaSystemAppearance -bool No
defaults write com.apple.SystemProfiler.AboutExtension NSRequiresAquaSystemAppearance -bool No
```

</details>

<details><summary><h4>Show Hidden Files</h4></summary>

Does what it says on the tin. Shows all files, including hidden ones, in the Finder.

```sh
defaults write com.apple.Finder AppleShowAllFiles YES
killall Finder
```
</details>

<details><summary><h4>Show GPU Tab in Activity Monitor</h4></summary>

Unhides the hidden sECrET GPU tab in macOS' Activity Monitor, helpful for seeing which apps are running on what GPU!

```sh
defaults write com.apple.ActivityMonitor ShowGPUTab -bool true
```
</details>

<details><summary><h4>AirDrop over Ethernet</h4></summary>

Makes AirDrop scan Ethernet too!

```sh
defaults write com.apple.NetworkBrowser BrowseAllInterfaces 1
killall Finder
```
</details>

<details><summary><h4>Frosted Glass Terminal Theme</h4></summary>

Some macOS eye candy.

```sh
curl -OL https://raw.githubusercontent.com/Coopydood/OpenCore-Z490E-CometLake/main/EXTRAS/HyperTerm.terminal
```

Import through Terminal's preferences.
</details>


***

## Gallery
<img src="https://github.com/user-attachments/assets/f1c438c6-95a3-4d1f-bfdf-f45f72579618" alt="big boi OptiPlex 7060 SFF" width="1050"/><br><br>
<img src="https://github.com/user-attachments/assets/100abfc8-5693-40c3-ad4f-7d47d36fe290" width="30%"></img> <img src="https://github.com/user-attachments/assets/77db9e21-9dd3-4434-b17f-8f60caececf4" width="60%"></img> <img src="https://github.com/user-attachments/assets/02b35032-f402-4ef9-98eb-6781bb0316bd" width="45%"></img> <img src="https://github.com/user-attachments/assets/e71d9a40-0e29-40e0-a2fe-b99fa6180575" width="45%"></img> <img src="https://github.com/user-attachments/assets/5c6e7c1a-c574-4b2f-9e0b-99db05cbd25e" width="45%"></img> <img src="https://github.com/user-attachments/assets/26b39fbd-9dd8-4e1c-b11e-6a6326ad6cb7" width="45%"></img> <img src="https://github.com/user-attachments/assets/d1fe1999-892c-4401-9ed8-7de72f0b1607" width="45%"></img> <img src="https://github.com/user-attachments/assets/c73fc263-3ed8-427d-b92f-0055ec4ba69c" width="45%"></img>

***

## Disclaimer

This repo is simply a dump of my current and up-to-date OpenCore stuff that I use on my machine. 

Feel free to use it as an example and modify it however you'd like, but please don't expect it to "just work" - because it *probably* won't.

***

## Contribute!

If you've found a way to make the configuration better, or have solved issues outlined in the **Problems** section, please share your changes on GitHub for us all to use! Thank you!
