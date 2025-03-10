# LED Lamp Driver Design and Development
#### Client Name: Dustin M

## Project Requirements
Design small, durable and power efficient (at least 85%) SMPS based LED driver with PWM dimming solution using rotary encoder with pleasant haptics.
The design overall should have EMC/EMI addressed to **pass FCC certification.**

The design will consist of three PCBs namely:
- Main PCB
- ALS PCB
- Power PCB
- LED Strip PCB
  
### Main PCB Requirements
The main PCB will consist of the main power and control circuitry with below features:
- The main microcontroller should exist on this PCB. Recommendation to use ESP32-H2 mainly due to matter integration support. Open to Engineer recommendation
- Should have terminal blocks (JST ZH Series, JST PH Series, Molex PicoBlade, Molex MicroBlade or similar) for interconnection with the **LED Strip** and **ALS PCB**
- The design for rotary encoder is to be referenced from Smart Knob since it offers the closest to desired solution and is available open source. However, this is open to Engineer recommendation. Some references are below:
[Reference-01](https://github.com/scottbez1/smartknob/)
[Reference-02](https://github.com/SeedLabs-it/smartknob-home-assistant-integration?tab=readme-ov-file)
- Rotary encoder will have an array of side firing indicator LEDs similar to those in the above projects that will turn on, if power is off and ambient light conditions are low.
 - Film grade dimming without flicker. [Reference Article](https://www.waveformlighting.com/film-photography/introducing-filmgrade-smoothdim-technology-gradual-and-smooth-led-dimming)

 ### Power PCB Requirements
 - Should have Mains AC to DC power supply circuitry (USA Standard)
 - Power supply must offer short circuit, over voltage and current protection, with either a user resettable fuse or hiccup protection.

### ALS PCB Requirements
- Should have ambient light sensing capability mounted remotely from the Main PCB
- Should have terminal blocks (JST ZH Series, JST PH Series, Molex PicoBlade, Molex MicroBlade or similar) for interconnection with the **Main PCB**.

### LED Strip PCB Requirements
- Should be able to drive a strip of 100 pixels similar to [this LED Strip](https://store.yujiintl.com/products/well24-dim-to-flamewarm-led-flexible-strip-1250k-3000k-human-centric-lighting?srsltid=AfmBOoq5EGoB9BZTL0uHWthwVENhlcGTCX8RunhhBDAsdl8qAi0HqJcI). The desired length of the strip will be 500mm +/- 50mm.
- LEDs are **Constant Current** and not **Constant Voltage**.
- Should have terminal blocks (JST ZH Series, JST PH Series, Molex PicoBlade, Molex MicroBlade or similar) for interconnection with the **Main PCB**.



