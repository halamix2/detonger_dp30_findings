# Detonger DP30 findings
---
I bought one of these, there's not much info about them online so I figured I could write down what I've found out

# Overview
* Company: Detonger, sometimes sold as Aibecy
* Model: DP30S (soimetimes calles DP30)
* Resolution: 203dpi
* Line width: 576 dots
* Max paper width: 80mm
    * supports 25mm/30mm/38mm/40mm/45mm/50mm/60mm/70mm/80mm
* Max paper diameter: 50mm
* Max print width 72mm
* Interface: BT + USB
* Print Speed: 20 - 50mm/s
* Command Set:
    * LPAPI®
        * seems like Detonger-made API, but I'm not soure if it's really copyrighted, this info was copied from the shop description
        * See [https://github.com/GemHu/LPAPI](https://github.com/GemHu/LPAPI)
    * [CPCL(Comtec Printing Ccc Language), now Zebra]()
    * [ESC/POS]()
* Battery Capacity: 7.4V 1500mah Lithium Battery
* Weight: 293g
* Size: 12.7 x 10.9 x 6cm
* Drivers: [https://drv.detonger.com](https://drv.detonger.com)
* Package content:
    * Label Printer
    * USB Cable
    * User Manual
    * 2x Paper Adjusting Plates?

# Hardware

* Artery AT32F415CBT7 SoC
    * ARM Cortex-M4
    * 150MHz frequency
    * 128KB flash
    * 32KB RAM
* Boya BY25D80A 1MiB (8Mb) EEPROM
* Barrot BR8051A01 Bluetooth chip
    * with 24MHz crystal
* PTC T5139A-HT Modtor driver


---
`echo 'hmm' | lp -d DP30 -o raw`
`cat fug.dt >> /dev/usb/lp2`
    