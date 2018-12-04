![alt text](https://i.imgur.com/1N4AZjE.png)

# ⚡⚡⚡⚡⚡⚡⚡ The Flux Capacitor ⚡⚡⚡⚡⚡⚡⚡ </br> (A dynamic Lightning Network point of sale device) 

## *"I slipped, hit my head on the sink, and when I came to I had a revelation!  A vision!  A picture in my head!  A picture of this!"*

The easiest way for a physical merchant to accept Lightning Network payments is to download a wallet on their phone. This project however uses current merchant behaviour as its rationale. Merchants tend to have purpose built hardware devices for accepting payments. Merchants also outsource the security of some services, such as email, website hosting, etc; restraints on time and technical ability make it unlikely for merchants to manage their own email servers. The assumption can be made that the majority of merchants are likely to engage similarly with LN, for this reason the Flux Capacitor is a simple, cheap device that can request and display a dynamic invoice from Lightning Network custodian Acinq Strike https://strike.acinq.co/. Once the amount of bitcoin earned over LN reaches a specified amount (ie 0.001BTC) Strike outputs the bitcoin to a mainchain address, ideally a hardware wallet. 

A merchant therefore, could accept bitcoin over LN using a Flux Capacitor, have the funds concatenate on Strike then have the funds root directly to their hardware wallet. The main security trade-off in such a system would be the funds held temporarily on Strike, but this would only be limited to a negligible amount.

Although the Flux Capacitor focuses on ease of access and current merchant behaviour, if the merchant were in the position where they wanted to switch to managing their own LN node, they could easily switch the Flux Capacitor to connect directly to an LN node.
