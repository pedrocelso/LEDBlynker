# LEDBlynker
A basic .ino file to allow WS2812B LED strip control with google assistant, IFTTT, and Blynk

### TL;DR;
I had this idea to have a voice controlled LED strip on my kitchen/bed, and after a LOT of research, I came up with this code and setup.

## Libraries
To run this project, you'll need to install 3 libraries:
1 - https://github.com/esp8266/Arduino
2 - https://github.com/blynkkk/blynk-library
3 - https://github.com/FastLED/FastLED

## Hardware Parts
1 - NodeMCU ESP8266
2 - WS2812B LED strip.
3 - Jumper Wires.
4 - 200 Ohm resistor (Optional: https://github.com/FastLED/FastLED/wiki/Power-notes#tips).
5 - Solderless breadboard (For prototyping. Optional).

## Schemas
Basically, there are 2 possible schemas for this, one, using the USB as power source for all the circuit, and other using an external power source.
On my longest strip, I have 65 LEDs, and according to the datasheet each LED on its full white/brightness should need 60mA. So:
```
65*0.06 = 3.9A
```
I would not be able to provide enough current to the strip, that's why I used an external power source, but to be honest, I didn't notice anything different when I switched the power input (My USB power supply ca provide 2.4A).

### USB as power source
![USB Schema](https://user-images.githubusercontent.com/2895204/51602286-e2644e00-1f06-11e9-93c8-f889d97f1247.PNG)

### External power source
![External Power](https://user-images.githubusercontent.com/2895204/51602378-0fb0fc00-1f07-11e9-8a35-563b6a3ff3c9.PNG)

