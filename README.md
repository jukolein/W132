<h1> Modification of a Ventus W132 to send both NMEA 0813 and NMEA 2000 datagrams </h1>

This repo describes the modification of a **[Ventus W132](https://de.elv.com/ventus-ersatz-windmesser-w132-fuer-funk-wetterstation-w155-w177-und-w137-124129)** replacement wind sensor, so it can send the NMEA 0813 information wirelessly or the NMEA 2000 via a CAN BUS.
![ventus](https://user-images.githubusercontent.com/16275519/137125907-6f76b55a-1524-4479-bf08-04bba0200843.jpg)
The original sensor for the angle gets replaced by an **[AS5600](https://www.ebay.de/itm/164267218236)** magnetic orientation sensor to achieve a better resolution. 
The computing an wireless transmission of the NMEA Datagrams as well as the web interface is done with an **[ESP32](https://www.az-delivery.de/products/esp32-developmentboard)**.
The NMEA 2000 data can be send via an **[SN65HVD230](https://eckstein-shop.de/WaveshareSN65HVD230CANTransceiverBoard33V2CESDProtection)**.

The modification reuses as many of the original components as possible, so that, theoretically, only a few parts are needed:
- an ESP32
- an AS5600
- a chamfered 5mm spring pin

And, for NMEA 2000,
- an SN65HVD230
- fur jumper wires

All the other components are taken from the original sensor. That reduces the overall costs to approximately 40€.

The firmware can either work standalone, where the sensor creates an access point that can be used to display the data on a tablet or phone without any further hardware, or be integrated in an existing setup.

This projecj is a continuation of the **[NMEA0182-Windsensor-project](https://github.com/jukolein/NMEA0183-Windsensor)**.

The firmware can either connect the sensor to an existing network or create an access point.
It has a graphical display of the data and a settings page in English and German.

<img src="https://user-images.githubusercontent.com/16275519/137125443-24283980-5bc1-4569-83f8-183af19cbef4.jpg" alt="drawing" style="width:500px;"/>

<img src="https://user-images.githubusercontent.com/16275519/137125304-1dc74a62-5a2b-493d-9867-e3cd8ebd91ed.jpg" alt="drawing" style="width:500px;"/>

