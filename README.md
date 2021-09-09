# Temperature-controlled-LEDs
LabVIEW project to light up different colored LEDs depending on the temperature.

**Setup**
1. Connect 5V power from the Arduino to the positive power rail on the breadboard
2. Connect ground from the arduino to the negative power rail on the breadboard
3. Wire three different colored LEDs to digital PWM connectors on the Arduino using a breadboard (note which LED is in which PWM connector)
4. Wire a TMP36 sensor into the breadboard, giving the left pin power and the right pin ground (the front is the flat side with the text) 
5. Wire the data wire (middle pin on the TMP36) to an anolog port on the arduino (note which anolog port was used)
6. In the LabVIEW program, select the COM port used by the arduino in the "Serial Port" dropdown
7. Enter the analog pin the TMP36 is connected to in the "Analog Channel" box
8. Enter the PWM pin for the cold LED, the room temperature LED, and the hot LED

**Usage**

Once everything is wired correctly, click the "Run" button in LabVIEW
If the temperature is 20C or below, the "Cold" LED turns on. 
If the temperature is between 21C and 24C, the "Room temperature" LED turns on.
If the temperature is 25C and greater the "Hot" LED turns on.

When one LED turns on, the others turn off.
