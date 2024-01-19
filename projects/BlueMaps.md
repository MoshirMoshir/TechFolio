---
layout: project
type: project
image: img/BlueMaps/BlueMaps.jpg
title: "BlueMaps"
date: 2023
published: true
labels:
  - HTML
  - CSS
  - Javascript
  - Game Dev
summary: "BlueMaps is an interactive map of the Blue Hole from Dave the Diver!"
---
<!---
<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>
-->
BlueMaps is an interactive map of the Blue Hole from Dave the Diver! It was created with a combination of HTML, CSS, and Javascript. 
Leaflet was used for the map function and the maps were created by datamining the game and opening the project files in Unity. 
Additionally, I recieved permission to include KlinkerKlank's original map which inspired this project.

```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [BlueMaps Repository Page](https://github.com/MoshirMoshir/BlueMaps).