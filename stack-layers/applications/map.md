---
description: Mobile Application Part
---

# 😇 MAP

### MAP Capabilities

#### Mobility Services

#### Operation and Maintenance

#### Call Handling

1. routing
2. managing calls
3. check subscriber status

#### Supplementary Services

#### Short Message Service

#### Packet Data Protocol (PDP)

#### Location Service Management Services

Location updating:

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
