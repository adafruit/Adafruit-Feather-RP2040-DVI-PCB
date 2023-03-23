## Adafruit Feather RP2040 DVI PCB

<a href="http://www.adafruit.com/products/5710"><img src="assets/5710.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit Feather RP2040 DVI. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/5710

### Description

Wouldn't it be cool if you could display images and graphics from a microcontroller directly to an HDMI monitor or television? We think so! So we designed this RP2040 Feather that has a digital video output (a.k.a DVI) that will work with any HDMI monitor or display. Note it doesn't do audio, just graphics!

It's kinda like we took our RP2040 Feather and DVI Breakout board and glued them together. You get all the pins for use on the Feather, the Lipoly battery support, USB C power / data, onboard NeoPixel, 8MB of FLASH for storing code and files, and then with the 8 unused pins, a DVI output that can be used with the PicoDVI library in Arduino or Pico SDK (note we don't have Circuitpython support for DVI output at this time)

In Arduino, which is what we recommend, we use our fork of PicoDVI to create an internal framebuffer of 320x240 or 400x240 16-bit pixels that is then continuously blitted out as pixel-doubled 640x480 or 800x480 digital video. Whatever you 'draw' to the internal memory framebuffer appears instantly on the digital display in crisp color. Since the library is a subclass of AdafruitGFX, it'll be familiar to folks who have used our TFT or OLED displays before.

Note that the DVI video generation uses one full core, both PIOs, and 150K (320x240) or 190K (400x240) of SRAM. It's kinda maxed out so be aware of the remaining resource limitations.

We also connected the HDMI-connectors I2C pins to the SDA/SCL of the Feather (through a safe level shifter) so you can read the EDID EEPROM of displays, and have broken out the CEC and Utility pads. The Hot Plug Detect pin is also available on the very end of the 16-pin header. Read this pin to know when a display has been connected!

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
