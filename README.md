![HooHooLa Project](./assets/HooHooLa.png)

Certain typs of owls use their facial muscles to turn from cute and fluffy to serious mode.
In the same way in this project the goal is to switch the peer to peer (P2P) network connection of interconnected cell phones and IoT sensors from the power saving [Bluetooth LE](https://www.bluetooth.com/bluetooth-le-primer/) to the higher performing [Wifi Aware](https://www.wi-fi.org/alternative-topologies).

The initial approach will be measuring [RSSI](https://www.networkacademy.io/ccna/wireless/interference-rssi-and-snr) and switching between the 2 mentioned techniques depending how big the value is, as the signal strength diminishes by the square of the distance in line-of sight situations and more than that in multipath situations, RSSI can be correlated directly to distance, which is the deciding factor for using either Bluetooth LE or Wifi Aware. 
A big part of the task will be to find suitable probabilistic metrics for the timing of the handoff between the 2 protocols.
Certain cases of drop off of RSSI need to be taken into account, see for instance the famous [RADAR](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/infocom2000.pdf) paper. The RSSI heavily depends phenomena like shadowing depending on the orientation of the body or if somebody suddenly puts his cell phone into his pocket. Also thinkable are effects like when walking between trees in a forest where the RSSI flucuates heavily depending on if trees are between compunication partners or not.

If we would do a change of communication protocol in all those situations, the network would be completely maxed out with constant handoffs.
Therefore the only suitable approach can only be to try to recognize the different situations and work with timeouts depending on if the RSSI is expected to recover immediately or not.

Additionally it is also thinkable to use additional metrics other than RSSI, which needs to be analyzed within that project.

For further details take a look at the currently open issues.