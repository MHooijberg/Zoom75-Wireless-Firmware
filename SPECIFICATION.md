# Hardware & software findings
This markup document describes the findings on the stock hard- and software specification.
This information is gathered by close hardware examination and reverse engineering the
stock firmware that comes iwth the keyboard.

## Table of Contents
[1. Hardware](#hardware)</br>
[2. Software](#software)</br>

## 1. Hardware <a name="hardware"></a>
This section describes the hardware specification.
If possible the information will include an external datasheet, model number and links.

### Battery:
**Source:** Meletrix</br>
**Modelnumber:** CL 3544105</br>
**Links:**

### Bluetooth board & WiFi:
**Source:** N/A</br>
**Modelnumber:** Unknown</br>
**Links:**</br>
**Notes:** The board did not have any recognizable marks,
specifications of this board is needed to do more development on the WiFi and Bluetooth module.</br>


### CPU:
**Source:** Firmware</br>
**Modelnumber:** AT32F415 RCT7-7</br>
**Links:**
 - [Datasheet](https://www.arterychip.com/download/DS/DS_AT32F415_V2.02_EN.pdf)

### Daughterboard:
**Source:** Meletrix</br>
**Modelnumber:** Ai03 C3</br>
**Links:**

### Memory:
**Source:** Firmware</br>
**Modelnumber:** w25q64</br>
**Links:**
 - [Potential Parts](https://www.digikey.com/en/products/base-product/winbond-electronics/256/W25Q64/339736)

### Printed Circuit Board (PCB:)
**Source:** Printed on board</br>
**Modelnumber:** WQ206A1UBTG1 V1.12 1723 KB81</br>
**Notes:** Pinouts / electrical schema is needed in order to make the firmware. Without it, it will be hard to write firmware.

## 2. Software <a name="software"></a>
The following section will contain information about the software, not all information is reliable
### Notes:
The following are notes on the findings on the stock firmware.

#### Operating System (OS)
The firmware seems to have an RTOS, this is indicated by a file path in the firmware "..\components\rtx\RTX_Conf_CM.c".
This indicates that the system might use CMSIS or CMSIS-RTOS by Keil a subsidiary of ARM Software.

It's also noteworthy to mention that the RGB animations are the same and in the same order as QMK's, this might mean they use the same library or similar code.
