### 
OpenCore EFI For Gigabyte B550 Aorus Elite AX V2 running MacOS Ventura.
----------------------------------------------------------------------
GUIDES:
----------------------------------------------------------------------
Guide: https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html

AMD specific guide (also for B550) : https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html

----------------------------------------------------------------------

SYSTEM INFO:
----------------------------------------------------------------------

--MotherBoard : Gigabyte B550 Aorus Elite AX V2 ( https://tinyurl.com/52ykzj4h )

--CPU : AMD Ryzen 5 5600 X

--GPU : ASUS Radeon RX 5600 XT 6GB GDDR6 TUF Gaming X3 Evo ( https://tinyurl.com/5bcvtddn )

--Nvme M.2 SSD : KINGSTON SNV2S500G 500Gb 

--Audio : Realtek ALC1200 codec

--Ethernet : Realtek 2.5GbE LAN chip

--Wi-Fi / Bluetooth : Intel Wi-Fi 6 AX200 - Bluetooth 5


BIOS Setup:
--------------------------------------------------------------------

    -Above 4G Decoding -> ON

    -Resisable Bar Support -> OFF 


OpenCore Info:
---------------------------------------------------------------------

    --OpenCore Version 0.8.9

    --MacOS Ventura 13.2.1

    --Opencanopy Minimal Theme : https://github.com/tekteq/opencanopy-minimal-theme

    --SMBios :  MacPro7,1 


Prior to install don't forget to change Device UUID,ROM,MB Serial,etc using GenSMBios https://github.com/corpnewt/GenSMBIOS





Kexts used :
---------------------------------------------------------------------

    -AppleALC

    -AppleMCEReporterDisabler

    -Lilu

    -LucyRTL8125Ethernet

    -MacProMemoryNotificationDisabler

    -NVMeFix

    -RestrictEvents

    -WhateverGreen


Note: These are the required kexts to boot with ethernet support ( no Wi-Fi , no Bluetooth ) just for the first installation.

Make sure you have connected your Ethernet cable for downloading MacOS in the Recovery.
       
In case there is no ethernet cable availiable, add AirportItlwm.kext ( https://github.com/OpenIntelWireless/itlwm/releases/tag/v2.2.0-alpha )
       currently on Alpha not tested in recovery.
       

Post Install :
----------------------------------------------------------------


Add Extra Kexts from Extra Kexts folder to the EFI/OC/Kexts

Extra Kexts folder contains kexts for Wi-Fi support , Bluetooth support and Power Management for CPU and GPU sensors.


Special Note :

      In the extra kexts folder there is a USBMap.kext which is specially for this particular Motherboard
       done using USBmap Python Script https://github.com/corpnewt/USBMap . Thanks to @corpnewt .
      If you don't have this MotherBoard do not add it and create your own USBMap.kext .




-Wi-Fi works with the alpha version of AirportItlwm for Ventura but it takes maybe 30-40 secs to connect.

-Bluetooth works 

-Continuity works from iPhone to Hack

-Handoff works from iPhone to Hack

-Audio works with no mic support. Using Bluetooth headphones or Airpods or a USB webcam with mic ,Mic works.



Dont't forget -- OC Snapshot of config.plist --  after addind the extra kexts.


TO DO: Update Opencore , Update Kexts




Cheers
       
       
       

<!--
**JohnLaz4/JohnLaz4** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on hackintosh...
- 🌱 I’m currently learning forever...
-->
