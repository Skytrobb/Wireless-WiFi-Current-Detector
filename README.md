# Wireless Wifi Current Detector

Detect current and display to a website using the nodeMCU. A split core transformer is used to detect current which 
is then read by the Arduino nodeMCU 3.3v analog-to-digital converter. the nodeMCU uses the ESP8266 which gives us the ability to create
a web server and display the acquired data. Using AJAX and google charts API, the data is then plotted on a line graph and updated in 
real time. 

## Getting Started

1. clone the repository
2. open the .ino file and change the wifi username and password to your own wifi network
3. compile and upload to your nodeMCU
4. in the Arduino IDE go to Tools > ESP8266 sketch data upload
5. wait for SPIFFS to complete and enjoy

### Prerequisites

Go here to set up your Arduino IDE for use with the ESP8266:
https://learn.adafruit.com/adafruit-huzzah-esp8266-breakout/using-arduino-ide

you will need a split-core non-invasive current detector and design a circuit that meets your needs as seen here:

https://learn.openenergymonitor.org/electricity-monitoring/ct-sensors/interface-with-arduino?redirected=true
*Example: my circuit was designed to detect current from 0-10A so I needed a 220 ohm burden resistor.


## Deployment

* Clip your split-core transformer to any wire with alternating current. You must separate ground from neutral and clip to only one wire or the two current will cancel out
* to find calibration factor for the energy monitor function use this function Rated Current/(AREF/2).
* Example: my circuit is rated to measure 10A max and my nodeMCU uses a 3.3v ADC. 10/(3.3/2) - 6.06


## Authors

* **Skyler Robbins** - *Initial work* - [skytrobb](https://github.com/skytrobb)


## Acknowledgments

* Thanks to circuits for you for doing the heavy lifting. I used a lot of their code and modified it as needed for my project

* https://circuits4you.com/2016/12/16/esp8266-web-server-html/

