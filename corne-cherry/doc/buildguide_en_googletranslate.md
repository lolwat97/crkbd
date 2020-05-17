# Build Guide

This is the Corne Cherry build guide.
[Click here for Corne Chocolate] (https://github.com/foostan/crkbd/blob/master/corne-chocolate/doc/buildguide_jp.md).


## Parts
### required
| Name | Number | Remarks |
|:-|:-|:-|
| PCB | 2 sheets |
| Top plate | 2 |
Bottom plate | 2 sheets | PCB type or acrylic type can be selected |
| ProMicro Protection Plate | 2 |
| ProMicro | 2 |
| TRRS Jack | 2 |
| Tact Switch | 2 |
| Diodes | 42 pcs | For chip components only |
| Kailh PCB Socket | 42 pcs | |
| Key switch | 42 pcs | Compatible only with CherryMX |
| Keycaps | 42 pcs | 1u 40 pcs, 1.5u 2 pcs |
| OLED Module | 2 |
| 4 pin headers | 2 |
| 4 pin sockets | 2 |
| Spacer M2 6.5mm | 10 pcs |
| Spacer M2 8mm | 4 pcs |
| Screw M2 4mm | 28 pcs | |
| Cushion rubber | 8 pcs |
| TRS (3 pole) cable | 1 pc | TRRS (4 pole) cable also possible |
| Micro USB cable | 1 |

### option
| Name | Number | Remarks |
|:-|:-|:-|
SK6812MINI | 54 pcs | Upward mounting 42 pcs, Downward mounting 12 pcs |

![01](https://user-images.githubusercontent.com/736191/54487431-789a6c00-48d9-11e9-9390-a8510b19ba34.jpg)

## Advance preparation
Although there is work to add a farm to ProMicro during implementation, it takes time to set up the environment for building the farm, so it is recommended to start first.
https://docs.qmk.fm/#/newbs_getting_started Refer to here and install the necessary ones according to the OS (installation is efficient because it takes time to install).

## Implementation

The PCB is reversible, so first decide which is left / right.

![02](https://user-images.githubusercontent.com/736191/54487432-789a6c00-48d9-11e9-87ea-3595b2f3ecc2.jpg)

### diode

Solder the diode of the chip part.
You can choose which side to attach to, but in this build guide, we will attach to the back side.
If you use [Tilting / Tenting plate] (https://github.com/foostan/crkbd/blob/master/corne-cherry/doc/buildguide_tilting_tenting_plate_jp.md), be sure to attach it to the back side __.

Since the tip parts are very small, it will be easier to work with tweezers and counteraction tweezers.
** Since the mounting direction of the diode is fixed **, you can proceed smoothly by arranging the columns and rows for mounting and the direction of the diode in advance as shown in the following photo.

![03](https://user-images.githubusercontent.com/736191/54487433-789a6c00-48d9-11e9-991b-92264a793ec9.jpg)

The diode orientation is as follows. Install so that the "|||" mark on the chip part faces the "|" of the diode mark "| ◁".

![04](https://user-images.githubusercontent.com/736191/54487434-79330280-48d9-11e9-82be-a9d98803a417.jpg)

It is a trick to attach chip parts, but first place solder on the right side of the pad as spare solder.

![05](https://user-images.githubusercontent.com/736191/54487435-79330280-48d9-11e9-9138-525d8ee68144.jpg)

Next, solder one leg of the diode by melting the spare solder.
At this time, it is recommended that you use the counter-action tweezers so that you can hold the chip components firmly without exerting any force and you can concentrate on the alignment and soldering.
Also, if the soldering iron is too hot or the solder is touched too much, the flux contained in the solder may evaporate and clean solder piles may form, but since it can be repaired later, it is only necessary to attach parts at this point. It's okay.

![06](https://user-images.githubusercontent.com/736191/54487436-79330280-48d9-11e9-856e-f3f5b9f58414.jpg)

It is okay if the diode does not float when viewed from the side with one foot attached. If it floats, it can be cleaned by pressing the diode with tweezers or fingers and reheating the part soldered with a soldering iron.

![07](https://user-images.githubusercontent.com/736191/54487437-79330280-48d9-11e9-996d-a578e767c12c.jpg)

Then solder the other. A small amount of solder is enough, so be careful not to apply too much.
If you attach it too much, you can remove it with a suction line or by scooping with a soldering iron.

If the amount of solder on the pre-solder side is small, additional soldering may be repeated, and if there are hills, it may be cleaned by applying flux from above and heating.

![08](https://user-images.githubusercontent.com/736191/54487438-79cb9900-48d9-11e9-9280-dc72a2087307.jpg)

### TRRS jack, reset switch

Solder the TRRS jack and reset switch to the surface of the PCB as shown in the picture below.
In this build guide, the diode is attached to the back side, so it will be the opposite side.

![09](https://user-images.githubusercontent.com/736191/54487439-79cb9900-48d9-11e9-9a57-80697fa8b484.jpg)

### Jumpers and pin sockets for OLED modules
When using the OLED module, jumper as follows.
** Please jumper only the surface **.

The pin socket is also soldered on the same side.

![10](https://user-images.githubusercontent.com/736191/54487440-79cb9900-48d9-11e9-95a7-750251e83a89.jpg)

If the jumper doesn't work, the amount of solder is probably low or the flux contained in the solder has evaporated.
In that case, use a large amount of solder or apply a separate flux to make a jumper.

### ProMicro
Solder the pin header so that it fits into the white frame, and then solder the ProMicro backside up.

![11](https://user-images.githubusercontent.com/736191/54487441-79cb9900-48d9-11e9-9317-e77c4c408a4f.jpg)
![12](https://user-images.githubusercontent.com/736191/54487442-7a642f80-48d9-11e9-85f6-469d8beaa9c0.jpg)

If you want to use spring pin header, please refer to [Helix build guide] (https://github.com/MakotoKurauchi/helix/blob/master/Doc/buildguide_jp.md#pro-micro).

### OLED module
Insert the pin header into the pin socket for OLED first, and then solder the pin header and OLED module.
At this time, the OLED module easily floats, so be careful not to float it while pressing it with your fingers.

![13](https://user-images.githubusercontent.com/736191/54487443-7a642f80-48d9-11e9-818a-4913b8abe986.jpg)
![14](https://user-images.githubusercontent.com/736191/54487445-7a642f80-48d9-11e9-9bb0-f753a5e4720b.jpg)

### operation check
It is recommended to check the operation when ProMicro and the OLED module are attached (it will be difficult to isolate the problem if done at the end).

To check the operation, first insert the crkbd firmware into ProMicro by referring to the "Firmware" section below (be sure to insert it on both sides).

Check the operation by connecting the left hand side to a PC with MicroUSB and connecting the left hand side and the right hand side with a TRS cable. There may be a defect such as a jack, so be sure to connect the left and right, not one by one, and check the operation. If everything is done correctly up to this point, shorting the pad to attach the PCB socket with tweezers etc. will display the key pressed on the OLED module.

![15](https://user-images.githubusercontent.com/736191/54487446-7a642f80-48d9-11e9-8bd2-2b413e3e080a.jpg)

### Kailh PCB Socket
Fill the pads on both sides of the backside with solder. Since it is difficult to add it later, please add a large amount in advance.

![16](https://user-images.githubusercontent.com/736191/54487447-7afcc600-48d9-11e9-91cb-edd541365180.jpg)

Insert the socket, melt the solder you have, and attach it.
At this time, hold the socket with tweezers or fingers to prevent it from floating.

![17](https://user-images.githubusercontent.com/736191/54487448-7afcc600-48d9-11e9-8e72-0449937a2310.jpg)

Soldering is now complete.
If you want to attach an LED as an option, refer to the “LED” section below (it can be attached even after mounting the socket).

![18](https://user-images.githubusercontent.com/736191/54487449-7afcc600-48d9-11e9-9428-0b949a07afc4.jpg)

### Plates, switches

First insert the switch into the top plate.
You can do it later, but since it is necessary to insert some power into the switch, it is easier to put it in first.

![19](https://user-images.githubusercontent.com/736191/54487450-7afcc600-48d9-11e9-8160-de5b9c6a405b.jpg)

Finally, attach spacers with screws and cushion rubber at the four corners so that the top plate, PCB, and bottom plate are in order, and you're done.

![20](https://user-images.githubusercontent.com/736191/54487451-7afcc600-48d9-11e9-8c90-2f2919bf9483.jpg)

## Firmware
https://docs.qmk.fm/#/newbs_getting_started Please refer to here to prepare the environment for writing the firmware.

Once you have an environment, use the following command to build the firmware for Crkbd.

`` `
make crkbd: default
`` `

Execute the following command after the build is completed.

`` `
make crkbd: default: avrdude
`` `

When you execute it, you will see the log below and you can see that the number of `.`s is increasing.
During this period, press the reset switch ** twice ** to complete writing the firmware.

`` `
<Omitted>

Checking file size of crkbd_rev1_default.hex [OK]
 * File size is fine-27328/28672
Copying crkbd_rev1_default.hex to qmk_firmware folder [OK]
Detecting USB port, reset your controller now ........
`` `

Once the firmware has been written to ProMicro on one side, follow the same steps for the other.

That's it!

## LED (optional)
I will attach SK6812MINI.

SK6812MINI is very sensitive to heat and breaks easily.
We recommend using a soldering iron with a temperature control function and working at a temperature of 220 ° C to 270 ° C.
Also, even if you adjust the temperature, if you keep the iron on the LED for a long time it will be damaged, so try to solder as quickly as possible.
We solder four LEDs at a time, but it is recommended that you do not do four at a time and do two at a time to prevent the temperature of the LEDs from rising and it will be hard to break.

First, check the mounting position.

For 1 to 6, solder is performed so that the back side (Undergrow) is lit, and for 7 to 27, the front side (Backlight) is lit. The following is the position to install the LED.

![21](https://user-images.githubusercontent.com/736191/54487452-7b955c80-48d9-11e9-98f7-87490a584274.png)
![22](https://user-images.githubusercontent.com/736191/54487455-7b955c80-48d9-11e9-9498-c841747c5dbc.png)

For 1 to 6, when the black part surrounded by a circle is on the bottom as shown below, solder it so that the silk mark indicated by the arrow is on the top.
Please note that the direction changes between 1 ~ 3 and 4 ~ 5.

![23](https://user-images.githubusercontent.com/736191/54487456-7b955c80-48d9-11e9-8541-cecb8c7dc97b.png)

For 7 to 27, as shown below, solder the largest pad surrounded by a circle and the silk mark shown by the arrow next to each other.

![24](https://user-images.githubusercontent.com/736191/54487457-7b955c80-48d9-11e9-882d-59ff506d5f02.png)

If everything is soldered properly, it will glow as shown below.
If the LED does not light up halfway, the LEDs are connected in numerical order, so please suspect that the LED that does not light up or the LED in front of it does not have a soldering error or is damaged.

![25](https://user-images.githubusercontent.com/736191/54487458-7c2df300-48d9-11e9-9582-88a60d5b71c0.jpg)

This is completed.

![26](https://user-images.githubusercontent.com/736191/54487459-7c2df300-48d9-11e9-8f3c-2c480cef3b03.jpg)

# Build Guide

こちらは Corne Cherry のビルドガイドになります。
[Corne Chocolate はこちら](https://github.com/foostan/crkbd/blob/master/corne-chocolate/doc/buildguide_jp.md)。