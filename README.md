**Automatic Medicine Dispenser**

<p>
  <img src="./rep image 18.jpg">
</p> 
<p>
  Currently, older adults with dementia or general memory issues struggle to remember to take their medications and manage multiple medications. This means that these individuals may not take their medications at the correct times or at all and might need help from a caretaker. We want these individuals to be able to manage their medications independently and have confidence in themselves. Our project is a medicine dispenser that can be preloaded for a full week, including separate morning and night compartments, for a total of 14 functional compartments and 1 refill position. 
</p>

**Bill of Materials**
- 2 9V batteries  
- A small breadboard (you can use basically any breadboard as long as it accommodates the necessary design size) 
- A couple of different jumper wires (recommended package - [link](https://a.co/d/06EYdTq6)) 
- A USB Printer Cable
- An LED (depending on how much light you want, get as many LEDs).
- DC3V-12V DC Geared Motor (recommended package - [link](https://a.co/d/02fzENU2)) 
- 2 regular wires
- A cable to connect the battery 
- Resistor (higher than 222 ohms) 
- A 9V battery clip
- A DRV8833 Dual H-Bridge DC Motor Driver Module H
- 4 Hall Effect Magnetic Sensor Module 3144E  ([link](https://a.co/d/08p1yAlN))
- 32 Magnets, diameter of 5mm and depth of 2-3mm
- PLA Printer Filament Roll

**Required/Recommended Tools**
- Arduino-compatible coding program
- A soldering machine is not needed, but is suggested; it is commonly found in a library.
- A Rubber Mallet
- 3D Printer (originally designed for print on Prusa MINI)

**Mechanical Assembly**
<p>
  PS - The place in which you place your jumper wires to the breadboards, for example, for hall sensors, is based on how you coded into the Arduino. In this case, or if you are using the original code, the hall sensors go to pin number 2, 3, 4, 5, the buzzer to pin number 6 and then lead to 13. For an easier time, try to color coordinate. For example, as you will see in my design, I try to use black or darker jumper wires for ground, a lighter color such as yellow for power, and then medium colors such as blue and purple for signals.
</p>
1. For every hall sensor, using the male-to-female jumper wires, connect them to the hall sensor and buzzer, remembering which colors of wires go where (look in the picture for reference) <img src="./rep image 1.jpg">
2. Now connect the blue jumper wire (or whatever color you used) to the corresponding pin numbers (2, 3, 4, 5) and the purple jumper wire (buzzer) to pin number 6. <img src="./rep image 2.jpg">
3. Then, using the breadboard, align all the yellow jumper wire (power) on a single row then the black jumper wires on the row below it. <img src="./rep image 3.jpg"> <img src="./rep image 4.jpg">
4. If using the small breadboard, use two male to male wires to connect each row to the corresponding row next to it. <img src="./rep image 5.jpg">
5. Then connect the corresponding buzzer cable to power and ground. (In this case, power was connected through a white jumper cable and a brown cable for ground). <img src="./rep image 6.jpg">
6. Using male-to-male wires, connect one of the wires to 5V on the Arduino board and then to the power supply on the breadboard. Then connect one of the wires to GND on the Arduino board and then to the ground corresponding on the breadboard. (red is power and green is ground.) <img src="./rep image 7.jpg"> <img src="./rep image 8.jpg">
7. Then move on to the Dual H-Bridge; connect IN1​​ and IN2 to the corresponding pin number on the arduino board, pin 10 and pin 11. <img src="./rep image 9.jpg"> <img src="./rep image 10.jpg">
8. Using another male-to-female connector, connect GND from the dual H-bridge to one of the spaces on the row of GND on the breadboard.
9. Then using 2 wires, slowly strip some insulating part and tie and wrap the wires over the little flaps from the tip of the wire. Bonus points if you can solder them together for a stronger connection. <img src="./rep image 11.jpg">
10. Then use two female-to-female wires, to connect the wires to OUT1 and OUT2, connecting the whole motor to wires, (this doesn’t matter which one; it only determines which direction the motor spins) <img src="./rep image 12.jpg"> <img src="./rep image 13.jpg">
11. Use an additional male-to-male wire, to connect to the designated ground breadboard and connect it to an additional row on the breadboard (look at the image for an example; it is the blue wire) <img src="./rep image 14.jpg">
12. Then connect the black wire of the 9V battery clip to the row connected to GND of the Arduino board.
13. Using a male-to-female connector, connect the pin labeled EEP on the breadboard, then connect the red wire for the battery to it. (For more context, the white wire connects to EEP on board 2.) <img src="./rep image 15.jpg">
14. To connect the LED, using a male-to-male connector, connect the LED pin number, in this case 13, to the breadboard on an empty row. (This is so you have multiple LED pins and do not have to program or use additional pin numbers).
15. Connect both LED pins to a male-to-female jumper wire (making sure to remember which one is which); this is to make sure that the LEDs have more flexibility. In this case, the blue wire is the longer leg of the LED, and the black wire is the shorter leg of the LED. <img src="./rep image 16.jpg">
16. Then take a resistor and put one of the pins of the resistor to the row that connects to the LED pin number and one to the designated ground rows on the breadboards. <img src="./rep image 17.jpg">
17. Then connect the LED to both the designated ground row and the LED row. Connect the wire with the shorter leg (cathode) to a GND row and the longer leg (anode) to the row that connects to the LED pin number.
18. To start, get the code file from above, then plug the USB printer cable into the Arduino board and back into your computer (based on the circuit board you are using, you might need a different cable to connect your circuit board to your computer).

**3D Print and Assembly**
1. Print Settings: Final Cycle Outer Box should be printed on its front face, with automatic paint-on supports. <img src="./rep image 20.jpg">
2. Print the <a href="./Final Cycle Outer Box.stl" download>Final Cycle Outer Box</a>
3. Print the <a href="./Final Cycle Wheel.stl" download>Final Cycle Outer Box</a>
4. Print the <a href="./Final Cycle Medicine Tray.stl" download>Final Cycle Outer Box</a>
5. Put magnets in the designated holes, using a mallet to fully insert. Ensure that each magnet is facing the correct way before fully inserting, preferably using the hall effect sensor to confirm it is activated. If a magnet is placed backwards, carefully use a heatgun to soften the surrounding plastic, then use a stronger magnet to pull it out of the hole. After this, you will most likely need to super glue the magnet back into place, since the hole will no longer be a snug fit. If the magnets are too small, you can super glue them into place. <img src="./re image 19.img">
6. Trim down the motor shaft so the wheel does not excessively protrude out the front of the outer box.
7. Insert the motor shaft through the back of the outer box and into the back of the wheel. You may choose to glue the shaft into its socket on the back of the wheel, but only do this if you are certain the wheel is not excessively protruding out the front.
8. Secure the motor in place on the back of the outer box, ensuring the shaft is perpendicular to the back of the outer box. You may use tape, glue, or modify the outer box print to include a mount.

**Suggested Path to Functionality**
1. Attach the hall effect sensors to the back of the outer box in the positions where each magnet slot would align. Ensure the correct hall effect sensor placement based on the code and pins. Below is the approximate suggested location for positioning. <img src="./rep image 21.jpeg">
2. Add a door, latch, and hinge to the front of the box so that it can be opened for refill and closed to prevent medicine from falling out when upright and functional.
3. Add a door, latch, and hinge to the back of the box so that it can be opened for maintenance and closed during usage.
4. Modify code to release medication at the desired times of day.
