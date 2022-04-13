# Mods

> This section contains all my mods or parts created for the HevORT
>
> More mods from from other people can also be found here: [HevORT Documentation Mods section](http://docs.hevort.com/#/pages/mods/mods)

## Cooling

<grid>
  <item title="HD12/MGN12 CPAP Rapido Duct" image="docs/assets/images/HD12_MGN12_Rapido_Duct.png">
    <description slot="description">
      Fan duct for CPAP fan hose
      <br>(15mm inner diameter)
      <br><br>Mounts to the standard MGN12H/HD12 HextrudORT carriage
      <br><br>Requires:
      <br>- Standard: 4x M3x8mm screws
      <br>- UHF: 4x M3x14mm screws
    </description>
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="cad/HD12_MGN12_Rapido_Duct.step">CAD File</item-button>
    </buttons>
    <credits slot="credits">
      <credit name="MirageC">Initial work of MGN9 version</credit>
      <credit name="DonnerPlays">Modification to fit HD12/MGN12</credit>
    </credits>
  </item>
  <item title="HD12/MGN12H Rapido UHF Spacer" image="docs/assets/images/HD12_MGN12_Rapido_UHF_Spacer.png">
    <description slot="description">
      Spacer for the CPAP Rapido Duct
      <br>when the rapido is used with a volcano nozzle (UHF)
    </description>
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="cad/HD12_MGN12_Rapido_UHF_Spacer.step">CAD File</item-button>
    </buttons>
    <credits slot="credits">
      <credit name="MirageC">Initial work of MGN9 version</credit>
      <credit name="DonnerPlays">Modification to fit HD12/MGN12</credit>
    </credits>
  </item>
  <item title="HD12/MGN12 40mm fan mount (tested with Rapido hotend)" image="docs/assets/images/MGN12_HD12_Rapido_Fan_Shroud_40mm.png">
    <description slot="description">
      This bracket allows you to use a 40mm fan for
      <br>hotend cooling on the
      <br>MGN12/HD12 HextrudORT carriage
      <br><br>Includes small side openings to help with getting out the hot air and help with installation.
      <br><br>Is supported by two screws/flaps on the side
      <br><br>Requires:
      <br>- 3x M3x(8mm + fan size)
      <br>Example: 20mm thick fan = 28mm = 25-30mm
    </description>
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="cad/MGN12_HD12_Rapido_Fan_Shroud_40mm.step">CAD File</item-button>
    </buttons>
    <credits slot="credits">
      <credit name="MirageC">Initial work on version for Rapido with 25mm fan</credit>
      <credit name="DonnerPlays">Modification to allow 40mm fan to be used</credit>
    </credits>
  </item>
  <item title="CPAP 7040 part cooling solution" image="docs/assets/images/cpap_7040_solution/main.png">
    <description slot="description">
      Ability to mount a CPAP 7040 blower.
      <br><br>
      Also adds ability to change inlet direction using servo
    </description>
    <buttons slot="buttons">
      <item-button url="#/pages/mods/cpap_7040_solution.md">GitHub Page</item-button>
    </buttons>
  </item>
</grid>

## Extruder

<grid>
  <item title="BL-Touch Rapido UHF Hotend bracket"
        image="docs/assets/images/BL_Touch_Rapido_Hotend_UHF_Bracket.png">
    <description slot="description">
      Mounting bracket for the BL-Touch when used on a Rapido UHF hotend.
      <br>- Adds a lip on the top that prevents the support from rotating.
      <br>- Uses nuts for all screw holes instead of screwing into the plastic
      <br><br>Requires:
      <br>- 3x M3 nuts
      <br>- Main mounting screw: M3x(~35mm long screw)
      <br>- BL-Touch screws: 2x M3x8mm screw
    </description>
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="cad/BL_Touch_Rapido_Hotend_UHF_Bracket.step">CAD File</item-button>
    </buttons>
    <credits slot="credits">
      <credit name="MirageC">Initial work/version</credit>
      <credit name="DonnerPlays">Modification to use M3 nuts instead of threading into the plastic</credit>
    </credits>
  </item>
</grid>


## Other

<grid>
  <item title="ADXL345 mounting bracket on 40mm fan" image="docs/assets/images/ADXL345_40mm_Fan_Mount.png">
    <description slot="description">
      Allows you to easily mount an ADXL345 accelerometer to your print head.
      <br><br>Mounts to the front of a 40mm fan.
      <br>(tested with a 20mm thick fan)
      <br><br>Requires: 3.5mm longer screws
    </description>
    <buttons slot="buttons">
      <item-button icon="fa fa-download" url="cad/ADXL345_40mm_Fan_Mount.step">CAD
        File
      </item-button>
    </buttons>
  </item>
</grid>