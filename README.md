Hacking Bluetooth into a 20 y/o radio
=====================================


## TL;DR
	how to play music through original car's head unit by messing with the changer interface.


## what are we working with?
	- a stock 2002 Honda civic ES 
	- OEM head unit model: 651TA
	- compatible OEM CD changer model: 411CY
	- Bluetooth to AUX adapter XY-BT mini adapter
	- old junky IPhone car charger

## A little background.

``` plain
when I bought this car, I was looking into a way to bang my tunes in my new car.
The solution I came up with was a Bluetooth tape, yes they do exist.
```
![Bluetooth tape](https://github.com/mtsimmer/TsimmerMobileMusic/raw/main/img/BluetoothCassette.png)

## problems with the simple solution.

		* Forgetting to charge the cassette
		* Forgetting cassette on the charger
		* Stuck cassettes
		* Turning the cassette off to save battery 
		* Turning the cassette on every drive


The research
============

## possible solutions.
		* Solder Left and Right channels to the cassette magnetic head
				* +
						* It might work...
						* Pretty simple...
				* -
						* Tons of research regarding where to solder to 
						  the sources exist though there is service manual.
						* Pretty tough to find 5v power around it
		* Use the CD changer port.
				* +
						* Easy intrussion (only pin reconnections)
						* More info regarding third party changers
						* Existing implamintations of M-Bus (relavant for later)
						* Power is simple.
						* I own a CD changer.
				* - 
						* Dealing with high 12v Voltage
						* Simulating the functionality of a CD changer
		* Simulating a radio antenna.
				* + 
						* Single wire really simple
				* -
						* Fucking expensive.

My solution
===========

![Changer PinOut](https://raw.githubusercontent.com/mtsimmer/TsimmerMobileMusic/main/img/ChangerPinout.png)

## what to look for?
```mhm what we need```

``` plain
		
	- Actually worked pins
			* Pin 5  left
			* Pin 6  right
			* Pin 13 ground
			* Pin 14 ground 

	- Power (PROBLEM)
		* Pins 1,7 are constant, directly from the car batterry we dont wanna drain it
		* 2 accessory pin didn't work for me ```it should have though :((( ```
		* 8 for the smartasses, the illumination is not 12v it is dimmed for the inner part of the car
				```trust me I tried :(```

after determining the audio pins and realizing I don't have where to get 12v I went for the car socket connector.
```

Here is how the modded changer connector looks like.
====================================================

![FinalProduct](https://raw.githubusercontent.com/mtsimmer/TsimmerMobileMusic/main/img/FinalProduct.jpg)
