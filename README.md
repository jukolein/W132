<h1> Modification of a Ventus W132 to send NMEA0813 datagrams </h1>

This repo describes the modification of a **[Ventus W132](https://de.elv.com/ventus-ersatz-windmesser-w132-fuer-funk-wetterstation-w155-w177-und-w137-124129?utm_source=google&utm_medium=cpc&utm_campaign=Gshopping_de&refid=Gads&Gads_Shopping&gclid=CjwKCAjwtfqKBhBoEiwAZuesiOwKC0dxB-xq1Xj6LokchImPiAkdn1fCNTCBv3Svd9ZOriWCnDVgFhoCT0gQAvD_BwE)** replacement wind sensor, so it can send the information via NMEA0813.
The original sensor for the angle gets replaced by an **[AS5600](https://www.ebay.de/itm/164267218236)** magnetic orientation sensor to achieve a better resolution. 
The computing an wireless transmission of the NMEA0813 datagrams as well as the web interface is done with an **[ESP32](https://www.az-delivery.de/products/esp32-developmentboard)**.

The modification reuses as many of the original components as possible, so that, theoretically, only three parts are needed:
- an ESP32
- an AS5600
- a chamfered 5mm spring pin

All the other components are taken from the original sensor. That reduces the overall costs to approximately 30€.

The firmware can either work standalone, where the sensor creates an access point that can be used to display the data on a tablet or phone without any further hardware, or be integrated in an existing setup.

This project as a continuation of the NMEA0182-Windsensor-project. As it uses the same firmware please consult **[that manual](https://github.com/jukolein/NMEA0183-Windsensor)** for these questions. 
