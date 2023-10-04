Features of BLE 
- License free. 
- Supports multibrand mobile/GPOS.
- Low cost, and hence very much affordable. 
- Low power consumption which is very much needed in IoT infrastructure. 
- Not huge. 
- Good range coverage. 
- Extreme heterogeneity support



Topology
1. Broadcasting
	- broadcast like radio
	- 1 way communication
	- whichever device wants to pick the data will receive it
	- Broadcaster sends out "non connectable" advertising packets to all the devices that are willing to collect it
	- Observer will keep scanning at the pre-set frequency looking out to receive any non-connectable packets which are being broadcasted
	- only way to transmit data to more than one receiver at the same time
2. Connection
	- Uses a master slave configuration
	- A connection is permanent
	- 2 way communication
	- Master takes care of periodic data exchange 
	- Slave will keep sending connectable advertising packets, periodically . when there is an incoming request, it would be accepted by the slave to whom it is addressed.

STACK

Controller: Controller has the HCI, link layer and physical layer 

Host Controller Interface
- used to enable interoperability between hosts and controllers assembled by different manufacturers (increased heterogeneity). The same kind of interface is also available for host side.
- Link Layer (LL) defines packet structure.
- Physical Layer (PHY) takes care of the transmission/reception. Recollecting the OSI layer and physical layer's functionalities, same is applied here. Physical layer takes care of modulation/ demodulation. Physical layer is responsible for analog digital conversion.

Host: Now we describe the components of the host and their functionalities.
- Generic Access Profile (GAP) takes care of the device discovery, connection establishment, connection management and security. This layer is "MANDATORY" for all BLE devices.
- Generic Attribute Profile (GAIT) oversees the data exchange process. Whenever there is need to push data and to read or to write the data, the generic guidelines with respect to the process are governed by GATT.
- Attribute Protocol (ATT) is the protocol for accessing data.
- L2CAP, expanded as Logical Link Control and Adaptation Protocol, is responsible for fragmentation and de-fragmentation of the application data. Also, it administers the multiplexing and de-multiplexing of channels over the shared logical link. (Many regard this layer as Mux Layer.)
- Security Manager (SM) handles pairing, authentication, and encryption. Everything related to the security aspect is taken care here.
- Host Controller Interface (HCl): As in controller side, there is HCl for host side as well. The functionality remains the same as that in the controller.

Application Layer: Application layer is the topmost layer in BLE as in OSI. Application layer in BLE is responsible for User Interface (UI), Logic and Data Handling.
