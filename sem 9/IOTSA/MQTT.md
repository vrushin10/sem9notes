MQTT (Message Queuing Telemetry Transport) is a lightweight and efficient messaging protocol designed for low-bandwidth, high-latency, or unreliable networks. widely used standard in the Internet of Things (IoT) and other applications that require real-time communication between devices and systems. 

1. **Publish-Subscribe Model :** MQTT operates on a publish-subscribe messaging pattern, where clients communicate through a central broker. Publishers send messages to specific topics, and subscribers express interest in receiving messages from specific topics. This decouples the sender (publisher) from the receiver (subscriber), enabling efficient and scalable communication.

2. **QoS Levels :** MQTT provides three Quality of Service (QoS) levels:
    - QoS 0 (At most once): Messages are delivered once or not at all. There is no acknowledgment of receipt.
    - QoS 1 (At least once): Messages are guaranteed to be delivered at least once to the recipient but may be duplicated.
    - QoS 2 (Exactly once): Messages are guaranteed to be delivered exactly once. This level ensures message integrity but incurs higher overhead.

3. **Lightweight Protocol :** MQTT is designed to be lightweight and minimizes the overhead of the protocol itself, making it well-suited for resource-constrained devices and low-bandwidth networks.
    
In summary, MQTT is a lightweight, efficient messaging protocol based on a publish-subscribe model, offering different QoS levels to suit various communication needs. It is particularly well-suited for IoT and other applications where low bandwidth and reliable messaging are essential.



### CoAP
  
CoAP (Constrained Application Protocol) is a specialized protocol designed for the unique challenges of IoT (Internet of Things) and constrained device environments.

- CoAP offers a lightweight and efficient solution for communication
- CoAP is 1 to 1 communication protocol
- CoAP uses client server model
- CoAP is best on API REST model (one can call it restful)
- other protocol that depend on SOAP and can be referred as SOAPful 
- clients can used get put delete
- uses UDP for transmission 
- CoAP is connection less

CoAP operates on multiple layers 

1. **Application Layer**
2. **CoAP Messaging Layer**    
3. **Request/Response Layer**
4. **UDP**



## COAP vs MQTT

|Feature|MQTT|CoAP|
|---|---|---|
|Underlying protocol|TCP (connection oriented)|UDP (connectionless)|
|Communication model|M:N (many to many)|1:1 (one to one)|
|Power consumption|Higher than CoAP. Lesser than other protocols.|Lowest. Consumes less power than MQTT, making it the best.|
|Messaging model|Publisher/subscriber|Request/response (RESTful and not SOAPful)|

