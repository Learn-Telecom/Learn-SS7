---
cover: .gitbook/assets/8913c177-71d4-45a2-b2a5-13fa2fbb7066.webp
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# SS7 Signalling in Mobile Networks

## Welcome aboard!

Last weak got a new course and its time to add more notes about SS7 Stack (public) and some little details about SS7 Security.

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

RFS

{% embed url="https://academy.apistraining.com/node/8974" %}

### SS7 Introduction

* The overview of the SS7 system
* The definition and structure of the SS7 signalling network: SP, STP, SL, LS, etc.
* The logical division of SS7: MTP and User Parts
* Use of SS7 protocol in 2G and 3G mobile networks and fixed networks
* Overview of various SS7 protocols

### MTP – Message Transfer Part

* The functions of the different MTP levels
* The structure and functions of MTP signal units, signalling link states and link management functions
* MTP 3 message handling – addressing, routing, load sharing, and distribution
* The overview of Signalling Network Management and Testing functions

### ISUP – ISDN User Part

* Use and functions of ISUP in PSTN, ISDN, and mobile networks
* Various ISUP signalling procedures: call handling, circuit management, etc.
* ISUP messages and their structure

{% @mailchimp/mailchimpSubscribe %}

### SCCP – Signalling Connection Control Part

* SCCP functions and applications
* SCCP signalling modes: connectionless and connection oriented
* SCCP addresses and their usage in 3GPP networks
* SCCP messages and their structure

### TCAP – Transaction Capabilities Application Part

* TCAP functions and applications
* Functions of TCAP component and transaction sub-layer
* TCAP messages and their structure

### MAP – Mobile Application Part

* GSM/UMTS MAP interfaces and operations
* Overview of MAP signalling scenarios for mobility, call handling, supplementary services management, recovery, etc.
* Dialog portion functions

### Traffic case

* Detailed analysis of a mobile terminating call scenario with focus on MTP, SCCP, ISUP, TCAP, and MAP messages and their parameters

### CAMEL Application Part

* An introduction to Intelligent Networks nodes and functions with CAMEL as an example
* Overview of IN call triggers and CAMEL subscription information records
* Overview of basic CAP operations.

### SS7 over ATM

* Overview of SAAL-NNI protocols, their functions, and message formats
* Example SSCF and SSCOP procedures

### SS7 over IP

* Overview of SS7-over-IP interfaces, protocols, and emulation options
* Functions and messages of SCTP protocol, example SCTP packet flow
* Overview of M3UA functions and messages
* M3UA addressing with routing keys and routing contexts
* Example M3UA signalling scenarios for establishment of an association, user data transfer, and signalling network management.
