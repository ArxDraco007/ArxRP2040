# ArxRP2040 - A Custom DevBoard

## Why did I make this project?
Most devboards have limited usability. They don't fit every project. Therefore, it is best that there exists a board that is most customizable, adhering to the purposes that most projects need. This is a basic, very compact devboard that has 24 GPIO pins. This project gives a very good idea of the wiring of devboards and the parts needed to make your own.
This project can be built upon, adding additional parts, extending it, and adding the design.

## Pictures - 
<img width="1310" height="628" alt="image" src="https://github.com/user-attachments/assets/7c8ce831-71e3-4066-869b-47f6b90f6640" />
<img width="379" height="808" alt="image" src="https://github.com/user-attachments/assets/c22033d1-f4bd-4a67-a777-4f4f0bf016b0" />
<img width="330" height="797" alt="image" src="https://github.com/user-attachments/assets/67b5f44f-b18d-4430-9e68-b4f76373b21f" />
<img width="306" height="773" alt="image" src="https://github.com/user-attachments/assets/eb8ac1c5-9c32-423d-a9fd-db12a21089e1" />
<img width="624" height="867" alt="image" src="https://github.com/user-attachments/assets/fc030354-90b3-4ec9-bf40-3fd21536c47f" />

## How to make it?
Follow the schematic and wire the PCB.
Use the Image Converter in KiCad to convert your images to footprints to decorate your PCB.
Download the MicroPython .uf2 file for the RP2040 from micropython.org. Hold the BOOT button (SW1) while plugging in the USB. The board appears as a USB drive. Drag and drop the .uf2 file onto it. Use Thonny IDE or any serial terminal to upload main.py
Start by applying flux to the pads on the footprint where you'll be soldering. Tin one of the pads with a small amount of solder, then carefully place your component onto the footprint. Touch your iron to the tinned pad to reflow it and tack the component in place, then let go with your tweezers once it's sitting right. Move to the opposite pad and solder it properly to the component. Finally, go back to your first pad and add a bit more solder to make sure you've got a solid joint.

## Zine
<img width="1304" height="1999" alt="zine" src="https://github.com/user-attachments/assets/2dc3cfa7-d0bc-42b4-9636-6012e294dc4c" />

## BOM 
| Name | Purpose | Quantity | Total Cost (USD) | Link | Distributor |
|------|---------|----------|-----------------|------|-------------|
| RP2040 | Main MCU (QFN-56) | 1 | $1.00 | [Raspberry Pi]([https://www.digikey.in/en/products/detail/raspberry-pi/SC0914/13624793](https://www.raspberrypi.com/products/rp2040/)) | Raspberry Pi |
| MCP1700x-330xxTT | 3.3V 250mA LDO regulator (SOT-23) | 1 | $0.50 | [DigiKey](https://www.digikey.in/en/products/detail/microchip-technology/MCP1700T-3302E-TT/652676) | DigiKey |
| W25Q16JVZPIQ | 16Mbit QSPI NOR Flash (WSON-8) | 1 | $0.80 | [DigiKey](https://www.digikey.in/en/products/detail/winbond-electronics/W25Q16JVZPIQ/6193781) | DigiKey |
| USB-C Receptacle 14P | HRO TYPE-C-31-M-12 or equiv | 1 | $0.50 | [Hubtronics](https://hubtronics.in/usb-c-female-port?srsltid=AfmBOop8mfonTlbqSHLuMisYp1z4lderBX-p3EpFVBi8DrW3sMfJKgY2) | Hubtronics |
| Conn_01x20 header | 2.54mm 20-pin single row (J3 and J4) | 2 | $1.00 | [Mouser](https://www.mouser.in/ProductDetail/Amphenol-FCI/67996-420HLF?qs=QKvFUfBIyQIvQWWcVN8Heg%3D%3D) | Mouser |
| Conn_01x03 header | 2.54mm 3-pin SWD debug header (J2) | 1 | $0.20 | [Robu](https://robu.in/product/ds1021-03-1x3sf11-b-connfly-1x3-pin-2-54mm-pin-header-single-row-press-fit-type/) | Robu |
| SW_Push tactile switch | BOOT/RUN button (SW1) | 1 | $0.20 | [Digikey](https://www.digikey.in/en/products/detail/alps-alpine/SKRKAEE020/19529176) | Digikey |
| Crystal 12MHz GND24 | SMD 4-pad crystal 3.2x2.5mm (Y1) | 1 | $0.50 | [ETStore](https://www.etstore.in/products/d10953) | ETStore |
| Resistor 5.1K 0402 | CC pull-downs for USB-C (R1, R2) | 2 | $0.10 | [Mouser](https://www.mouser.in/ProductDetail/Vishay-Dale/RCC04025K10FKED?qs=Imq1NPwxi76qRPANg4q4sQ%3D%3D) | Mouser |
| Resistor 27R 0402 | USB D+/D− series resistors (R3, R4) | 2 | $0.10 | [Robu](https://robu.in/product/erj2rkf27r0x-panasonic-smd-chip-resistor-27-ohm-%c2%b1-1-100-mw-0402-1005-metric-thick-film-precision/) | Robu |
| Resistor 1K 0402 | General purpose (R5, R6) | 2 | $0.10 | [Mouser](https://www.mouser.in/ProductDetail/Vishay/CRCW04021K00FHEDP?qs=Vd2sgofiCLVNiwckQwwOyw%3D%3D) | Mouser |
| Resistor 10K 0402 | Pull-up (R7) | 1 | $0.05 | [Robu](https://robu.in/product/rc0402fr-0710kl-yageo-smd-chip-resistor-10-kohm-%C2%B1-1-200-mw-0402-1005-metric-thick-film-pulse-proof-high-power-pack-of-10/) | Robu |
| Capacitor 1uF 0402 | Bulk decoupling (C1, C10) | 2 | $0.20 | [Robu](https://robu.in/product/1uf-capacitor-smdc-0402-pack-of-50/) | Robu |
| Capacitor 0.1uF 0402 | Decoupling (C2–C9, C11, C12, C17) | 11 | $0.55 | [Robu](https://robu.in/product/0402yd104kat2a-kyocera-avx-smd-multilayer-ceramic-capacitor-0-1-%C2%B5f-16-v-0402-1005-metric-%C2%B1-10-x5r-avx-0402-mlcc/) | Robu |
| Capacitor 10uF 0603 | LDO bulk caps (C13, C14) | 2 | $0.30 | [Robu](https://robu.in/product/10uf-10000nf-50v-capacitor-0603-smd-package-pack-of-5/) | Robu |
| Capacitor 33pF 0402 | Crystal load caps (C15, C16) | 2 | $0.20 | [Robu](https://robu.in/product/mc0402n330j500ct-murata-smd-multilayer-ceramic-capacitor-33-pf-50-v-0402-1005-metric-%C2%B1-5-c0g-np0-mc/) | Robu |
| PCB 2-layer ENIG | JLCPCB, 5 boards | 5 | $18.00 | [JLCPCB](https://jlcpcb.com/) | JLCPCB |
| **Total** | | | **$24.30** | | |
 
