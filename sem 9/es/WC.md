# Unit 1 definitions
## The Cellular Concept

![[Untitled 4.png]]

###### **Cell**

Each cellular base station is allocated a group of radio channels within a small geographic area called a _**cell**_. eg A is a cell in the above diagram

###### **Cluster**

The _N_ cells which use the complete set of channels is called _**cluster**_

**OR**

The group of cells where the available frequency spectrum is totally consumed is called a cluster of cells

###### **Variables**

- S is the total number of duplex channels in a cluster
- K is the number of duplex channel in a cell
- N is the number of cells in a cluster
- M is the total number of times cluster is repeated in a cellular system
- C, aka Capacity, is the total the number of duplex channels in a cellular system
###### **Formula**
- K < S
- S = KN
- C = MKN = MS
- N = i² + ij + j²

here i = 3 and j = 2 
![[Untitled.png]]

##### **Channel Assignment Strategies**

- **Fixed channel assignment**
    - each cell is allocated a predetermined set of voice channel
    - any new call attempt can only be served by the unused channels
    - the call will be _blocked_ if all channels in that cell are occupied
- **Dynamic channel assignment**
    - channels are not allocated to cells permanently.
    - allocate channels based on request.
    - reduce the likelihood of blocking, increase capacity

**Handoff Strategies**

When a mobile moves into a different cell while a conversation is in progress, the MSC (Mobile switching center) automatically transfers the call to a new channel belonging to the new base station.

- identifying a new base station
- re-allocating the voice and control channels to the new base station.

#### **Handoff Operation**
![[Untitled 3.png]]

- **Handoff Threshold Δ**
    - Minimum usable signal for acceptable voice quality (-90dBm to -100dBm)
    - Handoff margin cannot be too large or too small.
    - If **Δ** is too large, unnecessary handoffs burden the MSC (Mobile switching center)
    - If **Δ** is too small, there may be insufficient time to complete handoff before a call is lost.
- Handoff must ensure that the drop in the measured signal is not due to momentary fading and that the mobile is actually moving away from the serving base station.
    
- Running average measurement of signal strength should be optimized so that unnecessary handoffs are avoided.
    - Depends on the speed at which the vehicle is moving.
    - Steep short term average signal strength -> the hand off should be made quickly.
    - The speed can be estimated from the statistics of the received short-term fading signal at the base station.
- **Dwell time:** the time over which a call may be maintained within a cell without handoff.

#### Handoff measurement
- In first generation analog cellular systems, signal strength measurements are made by the base station and supervised by the MSC.
    - In second generation systems (TDMA), handoff decisions are mobile assisted, called mobile assisted handoff (MAHO)
- Intersystem handoff: If a mobile moves from one cellular system to a different cellular system controlled by a different MSC.    
- Handoff requests is much important than handling a new call.

##### **Practical handoff consideration**

2 types of users :

1. high speed user with frequent handoffs.
2. low speed users that may never need handoff.

- Microcells are used to provide capacity, the MSC can become burdened if high speed users are constantly being passed between very small cells.
- Minimize handoff intervention
    - handle the simultaneous traffic of high speed and low speed users.
- Large and small cells can be located at a single location (umbrella cell)
    - different antenna height
    - different power level
- Cell dragging problem: pedestrian users provide a very strong signal to the base station
    - The user may travel deep within a neighboring cell
- Handoff for first generation analog cellular systems
    - 10 secs handoff time
    - is in the order of 6 dB to 12 dB
- Handoff for second generation cellular systems, e.g., GSM
    - 1 to 2 seconds handoff time
    - mobile assists handoff
    - is in the order of 0 dB to 6 dB
- Handoff decisions based on signal strength, co-channel interference, and adjacent channel interference.

## Paging system

![[Untitled 2.png]]

- Conventional paging system send brief messages to a subscriber.
- Modem paging system: news headline, stock quotations, faxes, etc.
- Simultaneously broadcast paging message from each base station (simulcasting).
- Large transmission power to cover wide area.