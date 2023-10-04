#### IOT Stack

![[Pasted image 20230823203638.png]](from bottom to top)

1. **Sensor/Physical Layer**
	- this mainly include sensors and actuators
	- example:- temp sensor, motor, servo, distance sensor etc.
2. **Processing and Control Action Layer**
	- this layer include the microcontroller / processor used 
	- examples of microcontroller include :- Arduino, NodeMCU, ARM dev boards
	- the os used also plays a major role 
	- examples of os include : android , Linux, iOS, RTOS like TinyOS
3. **Hardware interface layer**
	- this layer include the communication protocols used to communicate with different components or module e.g. WIFI module
	- e.g. of protocols CAN,SPI,i2c
4. **RF layer**
	- this layer includes the communication channel used for connecting to a bigger network or the internet eg Wi-Fi lifi RFID Bluetooth 
5. **Session Layer**
	- this contains general network networking guided by OSI model 
	- protocols used to send data between cloud and the device include MQTT, HTTP, CoAP etc.
6. **User experience**
	- this layer contains the software used by the end user and the user interface used for that 
	- this UI usually made using Object oriented programing language like java , JavaScript
7. **Application Layer**
	- Everything comes to perfection at this layer
	- Application layer talks about the possible applications which can be built with the support of rest of the layers. 
	- It can range from a simple automation application to smart city application.

"a ux should rather have p*** sites"

#### IOT Architecture
![[Pasted image 20230824005231.png]]
#### IOT Reference Architecture 
![[Pasted image 20230823221901.png]]
- The Physical Devices and Controllers 
	- The IoT reference model starts with physical devices and controllers that might control various devices. 
	- These are the “things” in the IoT, and they contain a wide range of endpoint devices that send and receive information. 
-  The Connectivity 
	- The connectivity is the most essential function of next stage is reliable, timely information transmission. 
	- The IoT reference model is for communications and processing to be carried out by existing networks.
- EDGE COMPUTING
	- This contains a small amount a data processing before sending it to cloud though gateway
	- The functions of third stage are driven by the need to convert network data flows into information that is appropriate for storage and higher stage processing at the fourth stage
	- for example converting raw sensor data into useable data that can be stored in a database
- The Data Accumulation
	- The data that is sent over the internet via gateways by the sensor nodes are obtained and stored in a database on the Cloud and the networking systems are built to dependably move data.
	- using protocols such as HTTP MQTT CoAP
- The Data Abstraction
	- The primary purpose is to get the compulsory and significant data out of all the data that is collected.
	- IoT systems will necessitate to scale to a corporate or even global level and will need several storage systems to accommodate IoT device data and data from conventional enterprise HRMS, CRM, ERP and other systems.
- The Application 
	- The analytics over the data and responding pursuant to the data to control the actuators at the sensor nodes is one of the primary applications of the IoT Architecture. 
	- The sixth stage is the application level, where information interpretation occurs. Software at this level interacts with fifth stage and data at rest, so it does not have to operate at network speeds.
- The Collaboration and Processes 
	- This is the seven stage of the IoT reference model. 
	- The human interaction and involvement in the IoT scenario are seen as the most neglected parts not only the device should be smart sufficient to perform certain tasks, but they should also have some intuitive interactions with the human.
	- One of the primary dissimilarity between the Internet of Things (IoT) and IoT is that IoT contain people and processes.
#### 3-Tier Architecture (IIOT Architecture)

- **Edge Tier:** It collects data from the edge nodes, using proximity networks. The architecture characteristics of this tier like nature of proximity networks, breadth of duration, etc. may vary according to specific cases.
- **Platform Tier:** Receives, processes and forwards control commands from enterprise to edge tier. It analysis data flow from the edge tier and other tiers. Provides management services to assets devices. 
- **Enterprise Tier:** It implements domain specific applications and provides interface to the end users. It receives data flow from edge and platform tiers. It also gives control commands to the platform tier for edge tier.

![[Pasted image 20230824004205.png]]


#### PRO CONS
##### Benefits of IIoT
- Digital/connected factory
- Facility management
- Production flow monitoring
- Inventory and supply chain management 
- Plant Safety and Security
- Quality control
- Packaging assessment
- Logistics and Supply Chain Optimization
- Real-time manufacturing data 
- Maintenance data
- Optimizing the manufacturing line
##### Drawback of IIOT
1. Cybersecurity risks. 
2. Technology challenges. 
3. Human resistance.
4. Cost.
#### M2M vs IOT
![[WhatsApp Image 2023-08-18 at 19.03.41.jpg]]




#### Gateway And Router
**High-quality IoT and IIoT routers for industrial applications.**
- These devices are able to manage and control complex connected environments by aggregating and transmitting sensor data, as well as translating communication protocols serving as a bridge between IoT devices and platforms
**Gateway**
- Gateway are physical network devices that allows the IOT devices to connect to a larger network or the cloud or the internet