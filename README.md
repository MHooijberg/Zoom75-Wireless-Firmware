<!-- Badges -->
[![Productpage](https://img.shields.io/badge/Official_product_page-_?style=flat&logoSize=auto&color=%23c3a372
)](https://meletrix.com/products/zoom75-collection)
[![Firmware branch](https://img.shields.io/badge/Firmware%20branch%20(experimental)-_?style=flat&logo=github&logoColor=%23fff&logoSize=auto&color=%23010409
)](https://github.com/MHooijberg/qmk_firmware/tree/meletrix_zoom75_wireless)
[![MCU Pull-request](https://img.shields.io/badge/MCU%20Pull--request-_?style=flat&logo=github&logoColor=%23fff&color=%23010409)
](https://github.com/qmk/qmk_firmware/pull/23445)
[![The Meletrix Discord](https://img.shields.io/badge/Join%20the%20discussion!-_?style=flat&logo=discord&logoColor=%23fff&logoSize=auto&color=%235865F2
)](https://discord.gg/meletrix-919202175530463272)
[![MIT License](https://img.shields.io/badge/License-MIT_License-yellow)](https://github.com/MHooijberg/Zoom75-Wireless-Firmware/blob/main/LICENSE)
[![Static Badge](https://img.shields.io/badge/DigiKey_schematics_in_Scheme--it-_?style=flat&logo=digikeyelectronics&logoColor=%23fff&color=%23CC0000)](https://www.digikey.com/en/schemeit/project/detail/73e2cde2b4834adca2eaaf81ed0ce7a5)


<!-- License -->

# Meletrix Zoom75 Wireless (The WQ206A1UBTG1 V1.12 1723 KB81 PCB)
This repository is meant for collaborative research on the Zoom75 Wireless keyboard by Meletrix. The goal is to establish opensource [QMK-based](https://qmk.fm/) firmware for the Zoom75 Wireless keyboard by Meletrix.

Meletrix markets the Zoom75 wired version as QMK compatible, however in order to add the wireless connectivity it required using a different MCU. The MCU thats in the Zoom75 Wireless is (highly likely to be the ArteryTek AT32F415 RTC7-7).

The current issue is that QMK does not have support for this particular type of MCU family. In order to add support ChibiOS needs to support this MCU so that QMK can make use of their Hardware Abstraction Layer (HAL) from the [ChibiOS-Contrib](https://github.com/ChibiOS/ChibiOS-Contrib) repository. After this a new PR with the MCU support needs to be submitted for review to both the [QMK Firmware](https://github.com/qmk/qmk_firmware) and and [QMK Toolbox](https://github.com/qmk/qmk_toolbox).

Note: It's important to note that if a QMK-compatible firmware is made for the keyboard, that it's only for the wired functionality. As QMK is very power consuming, that means that a better option to eventually add full wireless functionality that custom ZMK support should be made.
Creating ZMK firmware is a possible project in the future, and this repository will be updated with more information when this happens.

**Progress:**
- [x] ChibiOS support
- [x] QMK upstreamed ChibiOS
- [x] Submitted Pull-Request for adding MCU support to QMK for review.
- [ ] Gather information on the pinout for the board so that QMK can be configured properly.
- [ ] Submitted Pull-request for adding keyboard support to QMK for review.
