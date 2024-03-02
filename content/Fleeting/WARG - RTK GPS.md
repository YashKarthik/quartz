- Ardupilot has a list of supported GPS that communicate using NMEA protocol.
	- But they are expensive and GPS on sparkfun are better.
	- But we need to write our own firmware for it.

- Figure out what GPS we could use and how they're better than what we have right now,
	- What GPS do we use now?
	-  How does RTK?
	- GNSS vs GPS
		- GNSS is the general term for navigational sattellites.
		- GPS is the American constellation.
		- GNSS Devices can connect to different constellations for improved accuracy.
	- How many antenna
 
- GPS correction data formats 
	- How to transmit over mavlink.
	- Submit corrections over mavlink and ardupilot driver would unpack that and send it to the RTK capable GPS.
	- What correction data format does ardupilot use.
	- driver basically converts correction data from MAVLINk to whatever format the GPS uses
- tasks
	- research what all these terms mean
	- what can be used as a base station
	- make an arch doc
	- research what family of GPS to use (use the same protocol)
		- cheap stuff, expensive stuff,
		- long term what family do we want to invest our development time into
	- feel out what the space is like
	- get a gps
	- write ardupilot snf mission planner driver for it
     
1. Research COTS RTK solutions
2. Research RTK COTS software flow (how, what to edit in ardupilot).
3. Write ground station driver - mission planner.
4. Write ardupilot driver.
	1. Accept mavlink correction packets
	2. Unpack data.
	3. Send to RTK gps.

---

# GPS Frequencies
- L1, L2, L5 are the three civilian gps frequency bands.
	- L1: 1575.42 MHz
	- L2: 1227.60 MHz
	- L5: 1176.45 MHz
- L5 is the most accurate and is good at cancelling out ionosphere interference.
- But since we're planning on using RTK correction data, L1/L2 is also fine.

---

- https://discuss.ardupilot.org/t/big-gps-round-up/67755

Sub $200 RTK gpss
- Drotek DP0601 GNSS RTK F9P
	- $169 on [official store](https://store-drotek.com/891-rtk-zed-f9p-gnss.html)
	- [Datasheet](https://raw.githubusercontent.com/drotek/datasheets/master/DrotekDoc_0891B08A%20-%20DP0601%20GNSS%20RTK%20(F9P).pdf)
	- Comms: uart, spi, slave i2c, usb.
- mRo GPS u-Blox Neo-M9N – IST8308
	- Already have two of these on pegasus (or some variant of it).
	- $65-75 on [sparkfun](https://learn.sparkfun.com/tutorials/sparkfun-gps-neo-m9n-hookup-guide/all), $75 on [mRo](https://store.mrobotics.io/shoppingcart.asp)
	- Constellations: usa, russia, europe, china.
	- Supports Aurdupilot.
	- RTK:
		- It says not rtk ready, but...
	- Comms: uart, spi, i2c.
- MATEKSYS M8Q-5883 GPS Module
	- https://www.getfpv.com/matek-ublox-m8q-5883-gps-module.html
	- $35
	- Not sure if it supports Rtk.
	- Ardupilot compatible
- Allystar HD8040D L5 capable NMEA GPS with builtin antenna
	- Supposedly only $20.