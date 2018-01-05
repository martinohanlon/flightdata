# Piaware Flight Data Reader
## Martin O'Hanlon (martin@ohanlonweb.com)
## http://www.stuffaboutcode.com

## Description
A python 3 module to read flight data from the PiAware solution. 

[http://www.stuffaboutcode.com/2015/09/read-piaware-flight-data-with-python.html](http://www.stuffaboutcode.com/2015/09/read-piaware-flight-data-with-python.html)

## Structure
* flightdata.py - the flightdata python module

## Usage

	from flightdata import FlightData
	from time import sleep
	
	myflights = FlightData()
	while True:
		#loop through each aircraft found
		for aircraft in myflights.aircraft:
	
			#read the aircraft data
			print(aircraft.hex)
			print(aircraft.squawk)
			print(aircraft.flight)
			print(aircraft.lat)
			print(aircraft.lon)
			print(aircraft.validposition)
			print(aircraft.altitude)
			print(aircraft.vert_rate)
			print(aircraft.track)
			print(aircraft.validtrack)
			print(aircraft.speed)
			print(aircraft.messages)
			print(aircraft.seen)
			print(aircraft.mlat)
	
	sleep(1)
	
	#refresh the flight data
	myflights.refresh()

## Version history
* 0.1 - Initial stable version
