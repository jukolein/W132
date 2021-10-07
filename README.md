<h1> Modification of a Ventus W132 to send NMEA0813 datagrams </h1>

This repo describes the modification of a Ventus W132 wind sensor, so it can send the information via NMEA0813.
The original sensor for the angle gets replaced by an AS5600 magnetic orientation sensor to achieve a better resolution. 
The computing an wireless transmission of the NMEA0813 datagrams as well as the web interface is done with an ESP32.

The modification reuses as many of the original components as possible, so that, theoretically, only three parts are needed:
- an ESP32
- an AS5600 on a breakout-board
- a spring pin

All the other components are taken from the original sensor. That reduces the overall costs to approximately 30€.

The firmware can either work standalone, where the sensor creates an access point that can be used to display the data on a tablet or phone without any further hardware, or be integrated in an existing setup.
