# Temperature-controlled-LEDs
LabVIEW project to light up different colored LEDs depending on the temperature.

**Setup**
1. Connect 5V power from the Arduino to the positive power rail on the breadboard
2. Connect ground from the Arduino to the negative power rail on the breadboard
3. Wire three different colored LEDs to digital PWM connectors on the Arduino using a breadboard. The PWM wire will be the input for the LED. 
   The ground for the LED should have a 220K resister. (note which LED is in which PWM connector)
   
   ![Image of LED wiring](https://github.com/jfaulkner9292/Temperature-controlled-LEDs/blob/main/LED%20wiring.jpg?raw=true)
   
5. Wire a TMP36 sensor into the breadboard, giving the left pin power and the right pin ground (the front is the flat side with the text) 
6. Wire the data wire (middle pin on the TMP36) to an analog port on the Arduino (note which analog port was used)

   ![Image of TMP36 wiring](https://github.com/jfaulkner9292/Temperature-controlled-LEDs/blob/main/TMP36%20wiring.jpg?raw=true)

8. In the LabVIEW program, select the COM port used by the Arduino in the "Serial Port" dropdown
9. Enter the analog pin the TMP36 is connected to in the "Analog Channel" box
10. Enter the PWM pin for the cold LED, the room temperature LED, and the hot LED

   ![Image of TMP36 wiring](https://github.com/jfaulkner9292/Temperature-controlled-LEDs/blob/main/Temperature%20Controlled%20LEDs%20Front%20Panel.PNG?raw=true)

**Usage**

Once everything is wired correctly, click the "Run" button in LabVIEW
If the temperature is 20C or below, the "Cold" LED turns on. 
If the temperature is between 21C and 24C, the "Room temperature" LED turns on.
If the temperature is 25C and greater the "Hot" LED turns on.

Temperature is displayed in degree Celsius and degree Fahrenheit on the Front Panel.

The "Stop" button stops the program and displays the temperature at the time of stopping.

When one LED turns on, the others turn off.
