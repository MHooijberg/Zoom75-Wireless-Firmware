<img href="https://img.shields.io/badge/any_text-you_like-blue"></img>
# Meletrix Zoom75 Wireless (The WQ206A1UBTG1 V1.12 1723 KB81 PCB)
This repository is meant for collaborative research on the Zoom75 Wireless keyboard by Meletrix. The goal is to establish opensource QMK-based firmware for the Zoom75 Wireless keyboard by Meletrix.

## Introduction <a name="Introduction"></a>

### Tasks:
In order for the keyboard to be supported by QMK, the microcontroller (MCU) used in the keyboard must be one of the MCUs supported by QMK. If the MCU is not already supported, it needs to be added to ChibiOS, which involves submitting a pull request (PR) to extend ChibiOS support for that specific MCU. This is because the hardware abstraction layers of ChibiOS are used by QMK to talk to non-STM32 type MCU's. However this will also mean that existing features of the keyboard need to be manually added because these are not in QMK, for example the custom keycodes given by the company to manage connections to bluetooth, wired and wireless devices.

Also since Meletrix recommend their own firmware to flash the keyboard, there needs to be research done to check if the keyboard can be flashed safely through QMK's software.


