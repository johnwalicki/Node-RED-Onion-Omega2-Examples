# Node-RED Examples for the Onion Omega2+ / Omega2 Pro

[Onion](https://onion.io/) Omega2+ / Omega2 Pro Node-RED flows running on a $5 single board computer!

### Introduction

These Node-RED recipes for the Omega2+ / Omega2 Pro demonstrate:
- Hello World
- Send Random Numbers 1-100 to Watson IoT Platform, the Omega2+ OLED display, and LEDs
- Send CPU stats from the Omega2 Pro to Watson IoT Platform
- Display hourly Weather report from IBM Cloud on the Omega2+ OLED display
- Send GPS coordinates to Watson IoT Platform and the Omega2+ OLED display
- The IBM Cloud flow that sends / receives the Omega2+ MQTT events

### Learning Objectives

- Learn how to install Node-RED on the Omega2 Pro
- Create Node-RED flows that execute on the Onion Omega2 devices
- Send data from the Omega2 edge device to the IBM Cloud and Watson IoT Platform
- Receive commands and data from IBM Cloud and display information on the Omega2 LED 

### Prerequistes

- [Install Node-RED](https://github.com/OnionIoT/Onion-Docs/blob/master/Omega2/Documentation/Doing-Stuff/node-red.md) on the Omega2 Pro
- Once Node-RED is installed, several additional Node-RED nodes will be necessary. Install the following nodes using the npm command line.
- To install additional Node packages with Node-RED,  install NPM:
  ```
  # opkg update
  # opkg install node-npm
  ```

- Install **node-red-contrib-cpu**
 ```# node --max_old_space_size=512 $(which npm) -g install  node-red-contrib-cpu```
- Install **node-red-contrib-ibm-watson-iot**
 ```# node --max_old_space_size=512 $(which npm) -g install node-red-contrib-ibm-watson-iot```
- Register for a free [IBM Cloud](https://cloud.ibm.com/registration?cm_mmc=ibmdev-_-omega2-_-gitbhub-_-jwalicki) Lite Account
- Log into [IBM Cloud](http://cloud.ibm.com)
- Create a [Internet of Things Platform Starter](https://cloud.ibm.com/catalog/starters/internet-of-things-platform-starter) 


## Download

- There are screenshots posted so you can see the Node-RED flows
- If you're interested in trying these recipes on your Onion Omega2+ / Omega2 Pro, import the flows [here](flows/OnionPro-NodeRED-examples.json)


## Node-RED flows in this repository:
This Hello World flow shows Node-RED running on the Onion Omega2+
![Hello World flow](screenshots/OnionOmega2-HelloWorld-NodeRED-flow.png?raw=true "Omega2 Hello World flow")
This flow sends Random Numbers from 1-100 to Watson IoT Platform, the Omega2+ OLED display and flashes the Omega2+ LED high/medium/low - red/yellow/green.
![Random Number flow](screenshots/OnionOmega2-SendData2WIoTP-NodeRED-flow.png?raw=true "Omega2 Random Num to Watson flow")
This flow uses the node-red-contrib-cpu node to send Omega2 Pro CPU stats to Watson IoT Platform
![CPU Stats](screenshots/Omega2Pro-NodeRED-WIoTP-CPU-flow.png?raw=true "Omega2 Pro CPU Stats flow")
This flow sends GPS coordinates to Watson IoT Platform and the Omega2+ OLED display
![GPS Coordinates flow](screenshots/OnionOmega2-GPS2OLEDWatsonIoT-NodeRED-flow.png?raw=true "Omega2 GPS Coors to Watson flow")
This flow receives the current Weather temp from the IBM Cloud / Watson IoT Platform and displays it on the Omega2+ OLED display.
![Weather flow](screenshots/OnionOmega2-WeatherReport2OLED-NodeRED-flow.png?raw=true "Omega2 Weather report from Watson flow")
This IBM Cloud flow shows the MQTT events being received and sent to the Omega2+
![IBM Cloud flow](screenshots/IBMCloud-OnionOmega2-sendreceive-MQTT-Events.png?raw=true "Omega2 IBMCloud Watson flow")
Watson IoT Quickstart screenshot that graphs the random numbers being sent from the Onion Omega2+.
![WIoTP Quickstart screenshot](screenshots/WatsonIoT-QuickStart-OnionOmega2-graph-MQTT-Events.png?raw=true "Watson IoT Quickstart graph of Omega2 data")

### Authors

- [John Walicki](https://github.com/johnwalicki)

___

Enjoy!  Give us [feedback](https://github.com/johnwalicki/Node-RED-Onion-Omega2-Examples/issues) if you have suggestions on how to improve this tutorial.

## License

This tutorial is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](http://www.apache.org/licenses/LICENSE-2.0.txt).
