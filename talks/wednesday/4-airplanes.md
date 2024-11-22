# Tracking Airplanes
*Guy Royse*

* About
  * github.com/guyroyse
* Stack
  * (software) radio -> aircraft -> event streams -> redis
* What is software radio?
  * Radio you plug into computer
  * Antenna samples frequencies
  * SER Equal (?) audio freq viz app
* Hardware
  * RTL-SDR
  * HF antenna
  * upconverter
* Software 
  * SDR# (Windows)
  * Gqrx SDR (Linux/RaspberryPi)
  * CubicSDR
  * SRDangel
* Data formats
  * Morse code (...-)
  * RTTY (radio teletype)
  * APRS (automatic packet reporting system)
    * Vehicles (w/ encoded location data)
    * weather stations
    * individuals 
    * Listened by individuals, repeaters, internet gateways
    * aprs.fi website
  * AIS (automatic identification system; ex transponders on cargo ships)
    * position (Lat/Lng, heading, speed)
    * vesselfinder.com
    * marinetraffic.com
  * ADS-B
    * automatic dependent surveillance broadcast
    * Every aircraft broadcasts at 1090 MHz
    * ICAO ID ex (A835AF) = Leon Musk
    * Callsign ex N628TS = Leon Musk
    * Altitude in feet
    * Speed in Knots
    * heading in degress
    * Location in lat/lng
    * dump1090 helps viz aircraft traffic
      * `dump1090 --net --interactive`
  * Water/gas meters
  * Tire pressure sensor in cars
  * Satellite images from NOAA satellites
* Stack
  * SBS1 -> node.js library
  * redis stack
    * JSON, search, probabilistic, timeseries
  * radio-ingestor -> radio-consumer -> flight-api -> flight-events -> flight-ui -> api-gateway
* Setup
  * Connecting
    * sbs1/redis node.js libraries
  * Wait for message
  * Process message
* streams
  * a stack of things that have happened, with data associated with them
  * add via redis to event stream
    * XADD <stream name>
  * read via redis
    * XREAD STREAMS <stream name>
  * In node.js
    * `redisClient.xAdd(stream, "*", data)`
  * Wait for message, process event, publish event
* Resources
  * redis.io/docs/stack

