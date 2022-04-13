# CPAP 7040 part cooling solution

<div style="display: flex; justify-content: center">
    <img alt="Main image" style="height: 20%" src="/docs/assets/images/cpap_7040_solution/main.png">
</div>

## Recommended seller/fan

[>>AliExpress<<](https://www.aliexpress.com/item/4000890953760.html)

## Description

This part allows to mount a CPAP 7040 fan.

It features a ball valve in the inside to allow sucking in air either from   
the print area or from inside the electronics enclosure.

> Designed to be mounted on a 3mm thick plate with a cutout based on the **Back Plate** part backside

> Designed to be used with a 15mm inner diameter CPAP hose with rubber pieces on both sides (inner diameter 22mm)  
> Example:
> 
> [>>Amazon Germany<<](https://www.amazon.de/gp/product/B089ZXFMD2)

A small 9G servo (**TowerPro MG90S**)   
and **klipper**'s servo control feature coupled with two simple **gcode_macro**'s to switch the inlet side.

![inside view](/docs/assets/images/cpap_7040_solution/inside.png)
![back view](/docs/assets/images/cpap_7040_solution/back.png)

## CAD File

[>Download CAD File<](cad/cpap_7040_solution.step)

## Parts (STLs)

|WARNING|
Note that stls shown here may not be up to date all the time.

The [CAD File](#cad-file) will have the latest updates & changes
|WARNING|

|INFO|
Every part (STL) required once (1x)!
|INFO|

<grid v-bind:config="{gridTemplateColumns: 'repeat(5, 1fr)'}">
  <item title="Valve Horn" image="docs/assets/images/cpap_7040_solution/stls/Valve_Horn.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Valve_Horn.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Servo Arm" image="docs/assets/images/cpap_7040_solution/stls/Servo_Arm.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Servo_Arm.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Front Plate" image="docs/assets/images/cpap_7040_solution/stls/Front_Plate.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Front_Plate.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Back Plate" image="docs/assets/images/cpap_7040_solution/stls/Back_Plate.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Back_Plate.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Valve Housing Bottom" image="docs/assets/images/cpap_7040_solution/stls/Valve_Housing_Bottom.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Valve_Housing_Bottom.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Valve Housing Top" image="docs/assets/images/cpap_7040_solution/stls/Valve_Housing_Top.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Valve_Housing_Top.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Valve Ball" image="docs/assets/images/cpap_7040_solution/stls/Valve_Ball.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Valve_Ball.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Bottom Valve Bracket" image="docs/assets/images/cpap_7040_solution/stls/Bottom_Valve_Bracket.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Bottom_Valve_Bracket.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Servo Horn" image="docs/assets/images/cpap_7040_solution/stls/Servo_Horn.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Servo_Horn.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Servo Bracket" image="docs/assets/images/cpap_7040_solution/stls/Servo_Bracket.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Servo_Bracket.stl">Download</item-button>
    </buttons>
  </item>
  <item title="Fan Bracket" image="docs/assets/images/cpap_7040_solution/stls/Fan_Bracket.png">
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="stls/cpap_7040_solution/Fan_Bracket.stl">Download</item-button>
    </buttons>
  </item>
</grid>

## Hardware required

### Screws

|INFO|
All Cylinder type!
|INFO|

| Diameter | Length (mm) | Amount |
|----------|-------------|--------|
| M2       | 8           | 2      |
| M2       | 10          | 4      |
| M3       | 6           | 1      |
| M3       | 10          | 14     |
| M3       | 12          | 10     |
| M3       | 14          | 1      |
| M4       | 40          | 4      |

|INFO|
1x servo type screw required as well
|INFO|

### Nuts

| Diameter | Amount |
|----------|--------|
| M2       | 6      |
| M3       | 15     |
| M4       | 4      |

## Klipper setup

1. Connect the **TowerPro MG90S** to one of the **GPIO** pins of your **Raspberry Pi**. 
   - Ideally the servo should be powered by **5V
2. Add this section to your ``printer.cfg``:
   ```klipper
    [servo my_cpap_servo]
    pin: rpi:gpio12
    maximum_servo_angle: 180
    minimum_pulse_width: 0.001
    maximum_pulse_width: 0.005
   ```
   - Make sure to set your correct **gpio** pin
   - Note that you may have to play with ``minimum_pulse_width`` and ``maximum_pulse_width`` to get the correct angle value for 45°
     - Make sure to first zero the servo by plugging it in before connecting it to the valve
   - Using gpio pins of the rpi requires you to set up your rpi as an mcu in klipper.   
     refer to [RPi microcontroller](https://www.klipper3d.org/RPi_microcontroller.html) for further instructions
3. Add these **gcode_macro**'s to your ``printer.cfg``:
   ````klipper
    [gcode_macro CPAP_PRINT_AREA]
    gcode:
    SET_SERVO SERVO=my_servo ANGLE=0
    SET_SERVO SERVO=my_servo WIDTH=0
    SET_SERVO SERVO=my_servo ANGLE=0
    SET_SERVO SERVO=my_servo WIDTH=0
    
    [gcode_macro CPAP_ELECTRONICS_AREA]
    gcode:
    SET_SERVO SERVO=my_servo ANGLE=45
    SET_SERVO SERVO=my_servo WIDTH=0
    SET_SERVO SERVO=my_servo ANGLE=45
    SET_SERVO SERVO=my_servo WIDTH=0
   ````
   - The double execution is required to make the servo move all the way and disable itself after reaching it.   
     Otherwise the servo may move the whole time and use up cpu time!