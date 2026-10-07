# Reflow Noveau
## An update for the Reflow Château reflow oven controller by Will Floyd-Jones

Back in 2015 Hackaday published a post about the [Reflow Château](https://hackaday.com/2015/02/02/reflow-chateau/), a DIY reflow oven controller that uses a capacitive touchscreen as user interface. It was better looking than the alternatives available at the time, but as time passed by it started to become obvious that the project was obsolete: there are issues about DC and AC power separation, the chosen SSRs were already EOL when the project was released, the Teensy 3.1/3.2 board used for the project was [EOL in 2023](https://www.pjrc.com/teensy-3-2-end-of-life/), not to mention problems with the code that needed some fixes.

Reflow Noveau is an attempt to update the hardware while keeping the firmware as similar as possible in function to the original. The current plan of action is:

### Hardware:

The idea is to provide at least two versions: one using the same style of SSRs used by the original Reflow Château, but using components that are readily available and using a more common footprint, which is larger; the second version removes the SSRs entirely from the board, preferring to use external puck-style SSRs. Also, the microcontroller board of choice will be changed to allow the choice for an ESP32-S3 Devkit or a Raspberry Pi Pico/Pico 2. The hardware is being designed by me on KiCad 10 and will be released when done using the CERN Open Hardware Licence.

### Firmware:

The firmware will be updated to be able to run on the newer microcontrollers. DISCLAIMER: I'm not a programmer by trade, and I haven't coded anything seriously in over 20 years. I do not like programming anymore, although it is a need for this project. That said, I will be using Claude to make the changes. If you have a strong stance against AI, feel free to grab the [original source code](https://github.com/VinnyCordeiro/ReflowChateau) and work with it. I will be closely testing Claude's output on real hardware to guarantee everything is working as it should. The Apache License was chosen because (a) it is more permissive than some of the alternatives; and (b) no one knows which license Will Floyd-Jones would have chosen. Since he made the code available I don't think he will mind that choice, as originally made by [ianlee74](https://github.com/ianlee74/ReflowChateau), the first person that uploaded the code into Github.
