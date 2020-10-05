# The following table shows how to wire the sensor to the Arduino.

Fingerprint Sensor	                  Arduino

VCC	                                  5V (it also works with 3.3V)

TX	                                  RX (digital pin 2, software serial)
RX	                                  TX (digital pin 3, software serial)
GND	                                  GND


# Installing the Adafruit Fingerprint Sensor Library

1.  Download ADAFRUIT fingerprint library:-   https://github.com/adafruit/Adafruit-Fingerprint-Sensor-Library/archive/master.zip

2.  Unzip the .zip folder and you should get Adafruit-Fingerprint-Sensor-Library-master folder

3.  Rename your folder from  Adafruit-Fingerprint-Sensor-Library-master folder to  Adafruit_Fingerprint_Sensor_Library folder

4.  Move the folder to your Arduino IDE installation libraries folder

5.  Finally, re-open your Arduino IDE

# Enroll a New Fingerprint

Having the fingerprint sensor module wired to the Arduino, follow the next steps to enroll a new fingerprint. Make sure you’ve installed the Adafruit Fingerprint Sensor library previously.

1. In the Arduino IDE, go to File > Examples > Adafruit Fingerprint Sensor Library > Enroll.

2. Upload the code, and open the serial monitor at a baud rate of 9600.

3. You should enter an ID for the fingerprint. As this is your first fingerprint, type 1 at the top left corner, and then, click the Send button.

4. Place your finger on the scanner and follow the instructions on the serial monitor.

5. You’ll be asked to place the same finger twice on the scanner. If you get the “Prints matched!” message, as shown below, your fingerprint was successfully stored. If not, repeat the process, until you succeed.

# Finding a Match

You now should have several fingerprints saved on different IDs. To find a match with the fingerprint sensor, follow the next instructions.

1. In the Arduino IDE, go to File > Examples > Adafruit Fingerprint Sensor Library > Fingerprint and upload the code to your Arduino board.

2. Open the Serial Monitor at a baud rate of 9600.

3. Place the finger to be identified on the scan.

4. On the serial monitor, you can see the ID that matches the fingerprint. It also shows the confidence – the higher the confidence, the similar the fingerprint is with the stored fingerprint.

# Installing the 0.96 inch OLED libraries

To control the OLED display you need the adafruit_SSD1306.h and the adafruit_GFX.h libraries. Follow the next instructions to install those libraries.

1. Open your Arduino IDE and go to Sketch > Include Library > Manage Libraries. The Library Manager should open.

2. Type “SSD1306” in the search box and install the SSD1306 library from Adafruit.

3. After installing the SSD1306 library from Adafruit, type “GFX” in the search box and install the library.

4. After installing the libraries, restart your Arduino IDE.

5. Run the code with any number of saved fingerprints.
