+++
title = "Introduction to the CAN Bus"
date = 2022-10-13
+++

[The main page](templates/index.html)

[List of articles](content/blog/_index.md)

<abstract>

The CAN (controller area network) bus in an automobile is the network that enables communication between the vehicle’s sensors and its various electronic control units (ECUs). Modern production cars can have as many as 70 or more ECUs (CSS Electronics, 2018), controlling the engine, airbags, anti-lock braking system, tail lights, entertainment system, and more. CAN itself is a message-based protocol standardized as CAN specification 2.0 in 1991 by multinational electronics and engineering company Bosch (Cook & Freudenberg, 2008).

The CAN bus in an automobile could be thought of as a noisy, crowded, slower version of a traditional Ethernet LAN (local area network), except that the traffic is mostly UDP (user datagram protocol), a connectionless transport protocol, rather than the TCP (transmission control protocol) traffic that dominates most web and client-server networks.

  It is worth noting that not all automobile control systems run over the CAN bus. In addition to multiple bus architectures for sensory and control automation, including LIN (local interconnect network), FlexRay, and MOST (media oriented system transport), there are several other networks present in modern automobiles (Wolf, Weimerskirch & Paar, 2004). These network connections can include Bluetooth, GSM/LTE cellular network connections, GPS navigation, satellite radio as well as vendor-specific systems like OnStar. Proposals have also been made for more secure network messaging systems to protect critical functions. In one promising example, Schmandt, Sherman and Banerjee (2017) proposed a modified message authentication protocol to address security gaps in networks like the CAN bus, but automotive manufacturers have been slow to adopt these technologies.

There are some advantages to using UDP for CAN bus automotive communications (Vector, 2016). For one, there are fewer communication delays and therefore less variation in communication timing because UDP does not require feedback from the receiver like TCP does. Another advantage is the ability to broadcast to all controllers and sensors in the controller area network, so that a change in an actuator, like the turn signal lever, can be reflected on the dashboard and carried out on the lighting circuit without requiring multiple direct wiring circuits. The CAN bus architecture allows all of these devices to communicate over as little as one pair of shared wires running to each sensor, actuator, or ECU.

CAN bus protocol messages are small (eight bytes or less at a time), with no explicit addresses in the messages, just a priority value (messages from the engine or brakes get higher priority than the air conditioning or audio player). Although there is some integrity protection, in the form of a checksum, and availability protection in the form of error handling and retransmission of lost messages, the CAN bus protocol was not built with modern security controls in mind.

<abstract/>
