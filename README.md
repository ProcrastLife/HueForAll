## Intro

This project is dedicated to replicating the official palettes found in the Philips Hue app and implementing them in WLED and Home Assistant.

## Method
1. Using the Hue Essentials app on PC to extract hex codes for the colors of each palette.

   Example: Extracted Soho hex colors - "FE2777", "FEA06F", "FE6F99", "8313FE", "66FEDB"

2. The extracted hex codes are then implemented using following the template found [here](https://kno.wled.ge/features/palettes/#custom-palettes). Also with the help of Discord.

   Example: 
   ```json
   {"palette":[0,"fe2777",63,"fea06f",127,"fe6f99",191,"8313fe",255,"66fedb"]}
   ```
   The numbers between the hex codes denote their positions on the custom palette, ranging from 0 to 255. Hex codes are replaced with lowercase letters.

## To-Do

- [ ] Complete all scenes.
- [ ] Develop an alternative palette using blocks of colors instead of gradients.

### WLED
- Implement a method to create a custom library containing all scenes.
- Decide whether to use palette colors in "blocks" or "gradients".
- Find a suitable effect.

### Home Assistant
1. Enable the application of palettes to light groups as scenes.
2. Ability to synchronize these scenes with Hue scenes using scripts, or automation. 

   *Example: When activating the "disturbia" scene, trigger the Home Assistant scene named "disturbia."*

## How To Use

**WLED:** Download up to **ten** *.json palettes and name them palette[0-9].json. Follow these instructions from WLED:

"it can be uploaded to the controller using the /edit page (http://[controller-ip]/edit). The controller must be rebooted (/win&RB) before the newly uploaded palettes will be available. After reboot, the custom palette(s) will be named ~ Custom [0-9] ~ in the Palettes section of the user interface." - [WLED Palettes Documentation](https://kno.wled.ge/features/palettes/#custom-palettes)
