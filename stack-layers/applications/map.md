---
description: Mobile Application Part
---

# 😇 MAP



### MAP Capabilities

**MAP** (Mobile Application Part) is part of the SS7 suite, enabling communication within cellular networks. It provides functionalities such as:

* **Location Management:** Tracks and updates mobile subscriber locations.
* **Handover Support:** Manages seamless transfer of calls between cells.
* **Authentication:** Ensures secure subscriber access to the network.
* **Call Handling:** Facilitates call setup, routing, and teardown.
* **SMS and USSD:** Enables sending/receiving of SMS and support for USSD services.
* \*\*Subscriber Data Management

#### Mobility Services

#### Operation and Maintenance

### Call Management System Features

* **Subscriber Status Check**: Allows the system to verify the subscription status of users.
* **Managing Calls**: Provides tools for organizing and controlling inbound and outbound calls.
* **Call Routing**: Directs calls to the appropriate destination automatically.
* **Call Handling**: Facilitates efficient answering, transferring, and holding

#### Supplementary Services

* **Call Forwarding**: Redirects incoming calls to another number.
* **Call Waiting**: Notifies users of an incoming call while on another call.
* **Caller ID**: Displays the caller's number before the call is answered.
* **Conference Calling**: Allows multiple parties to participate in the same call.

#### Short Message Service

* **Message Storage**: Stores messages for later retrieval.
* **Text Formatting**: Supports basic text formatting options.
* **Delivery Reports**: Notifies sender upon message delivery.
* **Bulk Messaging**: Facilitates sending messages to multiple recipients simultaneously.

#### Packet Data Protocol (PDP)

* **Session Management**: Manages setup, maintenance, and release of data sessions.
* **Data Transfer**: Ensures reliable transmission of data packets.
* **QoS Support**: Provides Quality of Service parameters for data sessions.
* **IP Address Allocation**: Dynamically allocates IP addresses for devices.

#### Location Service Management Services

* **Location Updating**: Regularly updates the network with the subscriber's location information.
* **Emergency Services Support**: Provides location information to emergency services.
* **Geofencing**: Triggers alerts when a subscriber enters or leaves a specified area.
* **Location Privacy**: Manages user consent for location-based services.

***

### Location updating

This operation package includes the operations required for location management procedures between HLR and VLR.

```ssml
locationUpdatingPackage-v3 OPERATION-PACKAGE ::= {
 -- Supplier is HLR if Consumer is VLR
 CONSUMER INVOKES {
 updateLocation}
 SUPPLIER INVOKES {
 forwardCheckSs-Indication} } 
```

Location cancellation:

This operation package includes the operations required for location cancellation and MS purging procedures between HLR and VLR and between HLR and SGSN.

```
locationCancellationPackage-v3 OPERATION-PACKAGE ::= {
 -- Supplier is VLR or SGSN if Consumer is HLR
 CONSUMER INVOKES {
 cancelLocation} }
```

### MAP Specifications

MAP for GSM (prior to Release 4) is specified by 3GPP TS 09.02 (MAP v1, MAP v2)&#x20;

MAP for UMTS ("3G") and GSM (Release 99 and later) is specified by 3GPP TS 29.002 (MAP v3)

### MAP Interfaces

<table><thead><tr><th width="117.33333333333331">Interface</th><th width="98">Device 1</th><th width="101">Device 2</th><th>Description</th></tr></thead><tbody><tr><td>B</td><td>MSC</td><td>VLR</td><td>MAP/B - Most MSCs are associated with a Visitor Location Register (VLR), making the B interface "internal".</td></tr><tr><td>C</td><td></td><td></td><td></td></tr><tr><td>D</td><td></td><td></td><td></td></tr><tr><td>E</td><td></td><td></td><td></td></tr><tr><td>F</td><td></td><td></td><td></td></tr><tr><td>H</td><td></td><td></td><td></td></tr><tr><td>I</td><td></td><td></td><td></td></tr><tr><td>J</td><td></td><td></td><td></td></tr></tbody></table>

### Application Contexts

{% embed url="https://www.etsi.org/deliver/etsi_ts/129000_129099/129002/15.05.00_60/ts_129002v150500p.pdf" %}

#### MAP Interface Descriptions

Below is a brief overview of each MAP interface type:

* **C Interface**: Typically connects the HLR (Home Location Register) to the GMSC (Gateway MSC). It is used to route calls to the destination network.
* **D Interface**: Links the HLR to the MSC. It is essential for subscriber management and call routing decisions.
* **E Interface**: Connects the MSC to the MSC Server. It ensures seamless call connectivity within different network domains.
* **F Interface**: Connects the HLR to the EIR (Equipment Identity Register). It is used to verify the status of mobile equipment.
* **H Interface**: Connects the VLR to other entities such as SGSN (Serving GPRS Support Node), supporting mobility management.
* **I Interface**: Links different GSN nodes within the network, assisting in the management of GPRS services.
* **J Interface**: Used between two different network operators' MSCs, facilitating international call routing and roaming.

These interfaces ensure the smooth operation and management of cellular networks, supporting communication and mobility functionalities.

#### G Interface Overview

The **G Interface** connects the VLR (Visitor Location Register) with the HLR. This interface is crucial for updating and managing subscriber-related information such as location updates, service requests, and authentication. It supports efficient data exchanges necessary for maintaining consistent service quality and availability across different network areas.

#### K Interface Overview

The **K Interface** links the GMSC (Gateway Mobile Switching Center) to the PSTN (Public Switched Telephone Network). This interface is pivotal for bridging mobile and landline communications, enabling users to make and receive calls across network boundaries. It handles the conversion and processing of call data between systems, ensuring efficient and reliable connectivity.

#### L Interface Overview

The **L Interface** serves as the connection between the MSC (Mobile Switching Center) and the EIR (Equipment Identity Register). This interface is responsible for verifying the identity of mobile devices within the network. By checking the IMEI (International Mobile Equipment Identity) numbers against the EIR, it helps in detecting and preventing the use of unauthorized or stolen devices, thus enhancing network security and integrity.

#### M Interface Overview

The **M Interface** connects the MSC (Mobile Switching Center) with the BSC (Base Station Controller). This interface plays a critical role in managing voice and data calls within the mobile network by controlling and setting up calls, handovers, and resource allocation. It ensures smooth communication and coordination between the radio network and the core network, facilitating seamless user experiences.
