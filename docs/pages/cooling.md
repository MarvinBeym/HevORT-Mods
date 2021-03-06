# Cooling

<script>
new Vue({
  el: ".grid",
  data: {
    items: [
        {
            title: "HD12/MGN12 CPAP Rapido Duct",
            image: "../images/HD12_MGN12_Rapido_Duct.png",
            description: `Fan duct for CPAP fan hose
                        <br/>(15mm inner diameter)
                        <br/><br/>Mounts to the standard MGN12H/HD12 HextrudORT carriage
                        <br/><br/>Requires: 
                        <br/>- Standard: 4x M3x8mm screws
                        <br/>- UHF: 4x M3x14mm screws`,
            download: "../cad/HD12_MGN12_Rapido_Duct.step",
            credits: [{name: "MirageC"}]
        },
        {
            title: "HD12/MGN12H<br/>Rapido UHF Spacer",
            image: "../images/HD12_MGN12_Rapido_UHF_Spacer.png",
            description: `Spacer for the CPAP Rapido Duct
                        <br/>when the rapido is used with a volcano nozzle (UHF)`,
            download: "../cad/HD12_MGN12_Rapido_UHF_Spacer.step",
            credits: [{name: "MirageC"}]
        },
        {
            title: "HD12/MGN12<br/>40mm fan mount<br/>(tested with Rapido hotend)",
            image: "../images/MGN12_HD12_Rapido_Fan_Shroud_40mm.png",
            description: `This bracket allows you to use a 40mm fan for
                        <br/>hotend cooling on the<br/>MGN12/HD12 HextrudORT carriage
                        <br/><br/>Includes small side openings to help with getting out the hot air and help with installation.
                        <br/><br/>Is supported by two screws/flaps on the side
                        <br/><br/>Requires:
                        <br/>- 3x M3x(8mm + fan size)
                        <br/>Example: 20mm thick fan = 28mm = 25-30mm`,
            download: "../cad/MGN12_HD12_Rapido_Fan_Shroud_40mm.step",
            credits: [{name: "MirageC"}]
        },
        {
            title: "CPAP 7040 fan mount with inlet selector",
            image: "",
            description: `WIP`,
            download: "",
            hide: true,
        },
    ]
  }
})
</script>

[grid-template](../templates/grid-template.md ':include')