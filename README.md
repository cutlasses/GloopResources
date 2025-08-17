# GLOOP

<img src="https://www.thonk.co.uk/wp-content/uploads/2024/11/cutlasses-gloop-front-700x700.jpg" alt="Picture of Gloop module" width="300" height="300">


Gloop is a performance looper for Eurorack with the ability to playback recorded loops with 4 simultaneous play heads. This is the place to find all of the digital resources for Gloop.

To keep up to date with Gloop happenings, join the [mailing list](https://www.cutlasses.co.uk/cutlasses-instruments/gloop-update/)

## Documents
[Manual](https://github.com/cutlasses/GloopResources/blob/main/Manuals/Manual%201.3.0.pdf)  
[Thonk Product Page for Build Doc](https://www.thonk.co.uk/shop/cutlasses-gloop/)  

## Firmware

The firmware is what makes Gloop actually do anything. It's just like software on a normal computer, except it's permanent on the microcontroller until you update it. I hope to regularily update the firmware with new features and bug fixes.

Latest version is [here](https://github.com/cutlasses/GloopResources/blob/main/firmware/Gloop_1_3_0.bin) Click the "Download Raw File" button to download the raw file.

<img src="https://github.com/cutlasses/GloopResources/blob/main/images/Firmware%20download.png" alt="Picture of Github download button">



This will be used in the steps below.

## Testing

If you've built a DIY Gloop the test firmware should be installed by default, if not you can flash the test firmware found here https://github.com/cutlasses/GloopResources/blob/main/firmware/Other/GloopTest.bin

The firmware tests all of the components are working correctly. First it will run a screen test, look out for 'dead pixel' (i.e. little black dots when the screen if filled white), this could indicate a faulty screen. After the screen test you will you will be presented with a screen that looks like this:

<img src="https://github.com/cutlasses/GloopResources/blob/main/images/GloopTest.png" alt="Picture of Gloop Test firmware">

- **Row 1:** The status of the buttons - Menu Button, Record Button and Clear Button, 'u' means button is up, i,e, not pressed, 'd' means button is pressed down
- **Row 2:** The status of the encoders, shows -1 when turned left, +1 when turned right. Will also show a 'p' when the encoder button is pressed
- **Row 3:** Trigger input, shows 'on' when trigger is sent a trigger voltage, and 'off' otherwise
- **Row 4:** Shows the value of each of the CV inputs. From -5V/+5V, shown as a value from 0 to 100

You can now press the buttons, turn and press the encoders, and feed the module trigger input and CV. The module also passes through audio from the input to both outputs, A + B. You can give it an audio signal at the input and test the audio is coming out of A + B (at equals levels), you can use a speaker, or if you have one, an oscilloscope. You should make test the follow:
- each button shows 'd' when pressed (or 'p' for encoders)
- each encoder correctly registers left and right rotation
- each pot shows the full range from 0..99
- the trigger input correctly recognises triggers
- the CVs show the full range from 0..100, try giving them a slow lfo from -5v to +5v
- audio pass through - output waves match input waves in volume

If any of these tests fail, check your soldering and try again. If they still fail, contact Thonk support.

The code for this test is here https://github.com/cutlasses/GloopTest, it should also give a good starting point for writing your own replacement firmware for Gloop as it exposes a the hardware pin configuration.

### Flashing the Firmware

To update Gloop firmware, you need a USB micro-B cable and a firmware .bin file, follow these steps

Connect the Daisy Seed to your PC/Mac using the micro-B cable
- Connect the Daisy Seed to your PC/Mac using the micro-B cable
- Go to https://flash.daisy.audio/using Chrome
- Ensure ‘File Upload’ tab is selected
- Click ‘CHOOSE FILE’ and navigate to the firmware .bin file
- Click ‘FLASH’
- Hold the BOOT button down on the Daisy Seed, and then press and release the RESET button (this allows the Seed to be programmed via USB)
- The Daisy should appear in the window
- Click ‘Connect’and the firmware should start to flash

#### Windows Users
If you have difficulties flashing the Daisy, and it doesn't show up as a device as expected, see [here](https://github.com/electro-smith/DaisyWiki/wiki/Using-Zadig-to-Reset-USB-Driver-(Windows-Only)) 


