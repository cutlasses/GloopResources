# GLOOP

<img src="https://www.thonk.co.uk/wp-content/uploads/2024/11/cutlasses-gloop-front-700x700.jpg" alt="Picture of Gloop module" width="300" height="300">


Gloop is a performance looper for Eurorack with the ability to playback recorded loops with 4 simultaneous play heads. This is the place to find all of the digital resources for Gloop.

To keep up to date with Gloop happenings, join the [mailing list](https://www.cutlasses.co.uk/cutlasses-instruments/gloop-update/)

## Documents
[Manual](https://github.com/cutlasses/GloopResources/blob/main/Manuals/Manual%201.3.0.pdf)  
[Thonk Product Page for Build Doc](https://www.thonk.co.uk/shop/cutlasses-gloop/)  

## Firmware

The firmware is what makes Gloop actually do anything. It's just like software on a normal computer, except it's permanent on the microcontroller until you update it. I hope to regularily update the firmware with new features and bug fixes.

Latest version is [here](https://github.com/cutlasses/GloopResources/blob/main/firmware/Gloop_1_3_0.bin) Click the button to download the raw file. This will be used in the steps below.

### Testing

If you've built a DIY Gloop and want to test your Gloop you can flash the test firmware which allows you to test the screen and all of the buttons/switches/pots/encoders and sockets. https://github.com/cutlasses/GloopResources/blob/main/firmware/Other/GloopTest.bin

The code for this test is here https://github.com/cutlasses/GloopTest, it should also give a good starting point for writing your own replacement firmware for Gloop as it exposes a the hardware pin configuration.

### Flashing the Firmware

To update Gloop firmware, you need a USB micro-B cable and a firmware .bin file, follow these steps

Connect the Daisy Seed to your PC/Mac using the micro-B cable
- Go to https://electro-smith.github.io/Programmer/ using Chrome
- Hold the BOOT button down on the Daisy Seed, and then press and release the RESET button (this allows the Seed to be programmed via USB)
- Click the Connect button
- Select “DFU in FS mode”
- Click “Choose File” and browse to the firmware .bin you want to update Gloop to
- Click the Program button

#### Windows Users
If you have difficulties flashing the Daisy, and it doesn't show up as a device as expected, see [here](https://github.com/electro-smith/DaisyWiki/wiki/Using-Zadig-to-Reset-USB-Driver-(Windows-Only)) 


