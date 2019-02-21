
# ⚡⚡⚡⚡⚡⚡⚡ OpenNode Edition⚡⚡⚡⚡⚡⚡⚡ </br> (A dynamic Lightning Network point of sale device) 

## *"I slipped, hit my head on the sink, and when I came to I had a revelation!  A vision!  A picture in my head!  A picture of this!"*

Currently the Flux Capacitor focuses on ease of use, the concept being a small/cheap/low-powered device that can be given to merchants so they can start accepting lightning network payments. THe device connects to OpenNodes API in order to request and display LN charges.

Set up an account with OpenNode here:
https://opennode.co/join/f774f2a0-1377-45e2-b719-6b821f24900d

[![LN Slave Mod](https://i.imgur.com/vIvMD1p.jpg)](https://www.youtube.com/watch?v=yxiafO4Tc-A)

## Hardware needed

* ESP32 (without built in OLED!)
* Waveshare 1.54inch Epaper module
* LED (optional)
* Adhesive Arduino Keyboard
* Wires and stuff

## Notes

The project is written for the Arduino IDE, appropriate libraries in the includes will have to be downloaded separately.

I used a standard ESP32 board, recognised in the Arduino IDE as a "LOLIN D32", although the code could be fiddled to support most ESP32s (as long as they don't have an OLED screen!).

The trickiest part of the project was getting the ESP32 to build an appropriate byte-array image for the epaper from the QR code data - a more regular byte-array format, such as XBM, would not render correctly. https://javl.github.io/image2cpp/ was extremely helpful.

In order to get a smaller keypad I trimmed a very standard module availible online. As its a matrix, if care is taken, no functionality is lost in the surviving keys.

![SPI PINS image](https://i.imgur.com/6ERVnAr.jpg)

Epaper to ESP32 SPI connection example:
![SPI PINS image](https://i.imgur.com/zA1dRbD.jpg)

1.21 sends an ON to GPIO PIN 17 for 2 secs, which can be adjusted in the code: 

## Limitations 

I'm an imbecile. This project would not have been possible without the kind help from folks at Fulmo's lightning-network hackdays http://fulmo.org/. The project has been developed for demonstration purposes only, although it is surprisingly stable, and with a little work the project could be secure and production ready. 

## Possible future improvements 

* Access Point for setting WiFi + Strike key
