![alt text](https://i.imgur.com/1N4AZjE.png)

# ⚡⚡⚡⚡⚡⚡⚡ The Flux Capacitor ⚡⚡⚡⚡⚡⚡⚡ </br> (A dynamic Lightning Network point of sale device) 

## *"I slipped, hit my head on the sink, and when I came to I had a revelation!  A vision!  A picture in my head!  A picture of this!"*

The easiest way for a physical merchant to accept Lightning Network payments is to download a wallet on their phone. This project however uses current merchant behaviour as its rationale. Merchants tend to have purpose built hardware devices for accepting payments. Merchants also outsource the security of some services, such as email, website hosting, etc; restraints on time and technical ability make it unlikely for merchants to manage their own email servers. The assumption can be made that the majority of merchants are likely to engage similarly with LN, for this reason the Flux Capacitor is a simple, cheap device that can request and display a dynamic invoice from Lightning Network custodian Acinq Strike https://strike.acinq.co/. Once the amount of bitcoin earned over LN reaches a specified amount (ie 0.001BTC) Strike outputs the bitcoin to a mainchain address, ideally a hardware wallet. 

A merchant therefore, could accept bitcoin over LN using a Flux Capacitor, have the funds concatenate on Strike then have the funds root directly to their hardware wallet. The main security trade-off in such a system would be the funds held temporarily on Strike, but this would only be limited to a negligible amount.

Although the Flux Capacitor focuses on ease of access and current merchant behaviour, if the merchant were in the position where they wanted to switch to managing their own LN node, they could easily switch the Flux Capacitor to connect directly to an LN node.

[![LN Slave Mod](https://i.imgur.com/K9awdFf.png)](https://www.youtube.com/watch?v=Sa8v)

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

* Currency conversion!
* Access Point for setting WiFi + Strike key
