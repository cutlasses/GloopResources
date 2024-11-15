# GLOOP

Gloop is a performance looper for Eurorack with the ability to playback recorded loops with 4 simultaneous play heads. This is the place to find all of the digital resources for Gloop.

## Documents
[Manual](https://github.com/cutlasses/GloopResources/blob/main/ManualPDF.pdf)  
[Build Doc](https://www.thonk.co.uk/wp-content/uploads/2024/11/Cutlasses-Gloop-build-doc-v1.0.pdf)  

## Firmware

The firmware is what makes Gloop actually do anything. It's just like software on a normal computer, except it's permanent on the microcontroller until you update it. I hope to regularily update the firmware with new features and bug fixes.

Latest version is [here](https://github.com/cutlasses/GloopResources/blob/main/firmware/Gloop1_1.bin)

### Flashing the Firmware

To update Gloop firmware, you need a USB micro-B cable and a firmware .bin file, follow these steps

Connect the Daisy Seed to your PC/Mac using the micro-B cable
- Go to https://electro-smith.github.io/Programmer/ using Chrome
- Hold the BOOT button down on the Daisy Seed, and then press and release the RESET button (this allows the Seed to be programmed via USB)
- Click the Connect button
- Select “DFU in FS mode”
- Click “Choose File” and browse to the firmware .bin you want to update Gloop to
- Click the Program button


