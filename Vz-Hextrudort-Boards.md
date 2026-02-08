This project introduces convenient and useful PCBs designed for the [Vz-Hextrudort-Low](https://github.com/VzBoT3D/Vz-HextrudORT) and [Vz-Hextrudort-Plus](https://aliexpress.com/item/1005006121253410.html?shpMethod=CAINIAO_STANDARD&sku_id=12000036371654824&spm=a2g2w.stores.seller_list.3.317450c0yMkG1R)
Currently, there are no fully suitable toolboards for VzHextruders, as existing options require additional printed parts and are not 100% compatible with the [Vz-Printhead](https://github.com/VzBoT3D/Vz-Printhead-CNC)

# Prerequisites

Before installment, make sure you have suitable [X-Endstop mount](https://www.printables.com/model/1297201-x-endstop-mount)
Also, use proper hardware:
- M3x25 screw (for both extruders)
- M3x6 screw (Hextrudort-Low)
- M3x16 screw (Hextrudort-Plus)
- M3 standoffs (Equals for your motor length. You may also need 0.5 spacer for LDO motors)
# Boards

## [VzHextrudortLow](https://github.com/Rexsell/Vz-Hextrudort-Boards/tree/main/VzHextrudortLow "VzHextrudortLow") and [VzHextrudortPlus](https://github.com/Rexsell/Vz-Hextrudort-Boards/tree/main/VzHextrudortPlus "VzHextrudortPlus")

They are simple commutation boards, they require Molex Microfit 2x10 as an input. Just direct connection, simple yet useful.
![[Hextrudort-Low commutation board.png]]
![[Hextrudort-Plus commutation board.png]]
## [VzHextrudortPlusCan](https://github.com/Rexsell/Vz-Hextrudort-Boards/tree/main/VzHextrudortPlusCan "VzHextrudortPlusCan") and [VzHextrudortPlusUSB](https://github.com/Rexsell/Vz-Hextrudort-Boards/tree/main/VzHextrudortPlusUSB "VzHextrudortPlusUSB")
These are already CAN and USB boards respectively. USB version has several additional USB connectors for Beacon/Cartographer sensors and other devices. CAN board has only one CAN connector for external devices.

First of all, they are simpled version of toolboards. They were made as two-layer, singlesided PCBs in order to reduce cost and make them assemblable at home.
Secondly, CAN version I ordered and assembled two times, second one I corrected several mistakes. 
![[Hextruder Photo.png]]

Features:
- Onboard NTC sensor
- TMC2209
- Connectors for external probes
- Connector for FilGuard sensor (Supports simple endstop)
- MAX31865 (Only for USB version curently)
- Solder jumper to turn off power LEDs
- RGB LED for motor backlight (Only for USB)
- Molex Microfit 3.0 for heater
- PFET protection from reversed polarity
- 2 Fans connectors

## WARNING!!!

**Before using this project, double-check the hotnd sensor connector schematic. I experienced unstable readings due to this configuration. The cause could be poorly chosen components, suboptimal routing, or a faulty schematic. The issue was completely resolved after connecting the same PT1000 sensor to a MAX31865 board. I used the BTT EBB36 schematic as a reference, but I don't recall exactly how I selected the components — I may have chosen incorrect ones.**

## [VzLowCan-Pro](https://github.com/Rexsell/Vz-Hextrudort-Boards/tree/main/VzLowCan-Pro "VzLowCan-Pro")

It shares the same features (and issues) as the [VzHextrudortPlusUSB](https://github.com/Rexsell/Vz-Hextrudort-Boards/tree/main/VzHextrudortPlusUSB "VzHextrudortPlusUSB"). However, this version is adapted for the -Low model and includes several additional features, such as an extended configuration for the MAX31865 and a connector for a probe like the BL-Touch. It also has a jumper for fan voltage selection. The design is not yet finalized, but I believe more experienced engineers will be able to complete it.
![[VzLowCan-Pro.png]]