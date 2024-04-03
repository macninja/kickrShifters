# kickrSatelliteShifters
Da Wahoo ikke tilbyder satellit skiftere er dette mit forsøg på at lave dem.

## Dokumentation

Kan findes på [Wiki](https://github.com/macninja/kickrShifters/wiki)

## Referencer

[Stephen](https://github.com/StephenDone) har lavet et projekt hvor han bruger en Raspberry Pi https://github.com/StephenDone/kickr_shifters






## Arduino POC:
Tag et analog knaptryk sog send et digitalt signal
    Tag to analoge input og send til to forskellige digitale modtagere
    Send signalet imellem to Arduino via I2C
        Juster så adresse på slave og data kan justeres efter behov

## Spørgsmål:

### Hvordan finder jeg ud af hvilken enhed der er Master or hvilken der er slave?
### Hvordan finder jeg ud af spændingen der er i kredsløbet

Ifølge dokumentationen kan den max tage 3,5V
    
Here's a step-by-step guide on how to use a multimeter to identify the voltage supplied by the master device in an I2C circuit:

1. Prepare the Multimeter:
    * Set the multimeter to measure DC voltage. This is usually denoted by a V with a straight line (─) over a dashed line (~) symbol.
    * Choose an appropriate voltage range on the multimeter. If you're unsure of the voltage level, start with the highest range setting and adjust as needed.
2. Power On the Circuit:
    * Ensure that the I2C circuit is powered on and operational. This means that the power supply to the circuit should be connected and turned on.
3. Identify the SDA and SCL Lines:
    * Locate the SDA (Serial Data) and SCL (Serial Clock) lines on the I2C bus. These are the two signal lines used for communication.
    * If you're not sure which lines are SDA and SCL, refer to the documentation of your circuit or look for labels near the pins on the devices.
4. Set Up the Multimeter:
    * Keep the black probe (negative lead) of the multimeter connected to the common (COM) port.
    * Connect the red probe (positive lead) of the multimeter to one of the I2C bus lines, such as SDA or SCL. It doesn't matter which one you choose as long as you're consistent.
5. Measure Voltage:
    * Touch the tip of the red probe to the chosen I2C bus line (e.g., SDA).
    * Read the voltage displayed on the multimeter. This voltage indicates the voltage level supplied by the master device on the I2C bus.
    * Repeat the measurement process for the other I2C bus line (e.g., SCL) if necessary.
6. Interpret the Results:
    * Note the voltage readings obtained from both I2C bus lines.
    * The voltage readings should match because the master device typically provides the same voltage level to both SDA and SCL lines.
    * The voltage level you measure is the voltage supplied by the master device in the I2C circuit.
7. Document and Verify:
    * Record the voltage level you measured for future reference, troubleshooting, or documentation purposes.
    * If needed, verify the voltage level with the specifications or documentation of the master device to ensure accuracy.

By following these steps, you can use a multimeter to identify the voltage supplied by the master device in an I2C circuit.

Når Master/Slave er identificeret hvordan finder jeg slavernes adresse  
    Har hver greb forskellige adresser  
    Har alle venstre/højre greb samme knap adresser?  
Hvordan afkoder jeg det date der sendes fra slave til master  
Hvad sendes der fra master til slave  
Junctin boxen har 3 stik. Kan jeg bruge det frie stik til at sende blip kode

## Matrix Tastatur over I2C
https://www.hackster.io/venkatesh_rao/i2c-keypad-73a012

Keypad_I2C Library  
https://github.com/joeyoung/arduino_keypads/tree/master

Installing a Library on Mac OSX  
https://learn.adafruit.com/adafruit-all-about-arduino-libraries-install-use/installing-a-library-on-mac-osx

Add Managed Library to Arduino IDE  
https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-installing-a-library/
