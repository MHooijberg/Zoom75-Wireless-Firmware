# Meletrix Zoom75 Wireless (The WQ206A1UBTG1 V1.12 1723 KB81 PCB)
A repository dedicated for collaborative research aimed at establishing opensource QMK-based firmware for the Zoom75 Wireless keyboard by Meletrix.

---

# Table of Contents
[1. Introduction](#introduction)</br>
[1. Hardware](#hardware)</br>
[2. Software](#software)</br>
[3. Useful Links](#links)</br>

---

# Introduction <a name="Introduction"></a>

## Tasks:
In order for the keyboard to be supported by QMK, the microcontroller (MCU) used in the keyboard must be one of the MCUs supported by QMK. If the MCU is not already supported, it needs to be added to ChibiOS, which involves submitting a pull request (PR) to extend ChibiOS support for that specific MCU. This is because the hardware abstraction layers of ChibiOS are used by QMK to talk to non-STM32 type MCU's. However this will also mean that existing features of the keyboard need to be manually added because these are not in QMK, for example the custom keycodes given by the company to manage connections to bluetooth, wired and wireless devices.

Also since Meletrix recommend their own firmware to flash the keyboard, there needs to be research done to check if the keyboard can be flashed safely through QMK's software.

# Hardware <a name="hardware"></a>
This section describes information about the hardware.

## Battery:
**Modelnumber:** CL 3544105</br>
**Links:**

## Bluetooth board & WiFi:
**Modelnumber:** Unknown</br>
**Links:**

## CPU:
**Modelnumber:** AT32F415 RCT7-7</br>
**Links:**
 - [Datasheet](https://www.arterychip.com/download/DS/DS_AT32F415_V2.02_EN.pdf)

## Daughterboard:
**Modelnumber:** Ai03 C3</br>
**Links:**

## Memory:
**Modelnumber:** w25q64</br>
**Links:**
 - [Potential Parts](https://www.digikey.com/en/products/base-product/winbond-electronics/256/W25Q64/339736)

# Software <a name="software"></a>

## Notes:
The following are notes on the findings on the stock firmware.

### Operating System (OS)
The firmware seems to have an RTOS, this is indicated by a file path in the firmware "..\components\rtx\RTX_Conf_CM.c".
This indicates that the system might use CMSIS or 
CMSIS-RTOS by Keil a subsidiary of ARM Software.

It's also noteworthy to mention that the RGB animations are the same and in the same order as QMK's, this might mean they use the same library or similar code.

---

# Useful Links <a name="links"/>
