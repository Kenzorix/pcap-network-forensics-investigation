# Wireshark Analysis

## Objective

Initial packet-level analysis was performed using Wireshark to identify
unusual network communication and determine which traffic required
further investigation.

## Analysis Performed

- Reviewed packet conversations
- Examined source and destination hosts
- Reviewed DNS traffic
- Examined TCP/443 traffic
- Followed suspicious communication for further analysis
- Identified traffic requiring deeper investigation with Zeek

## Key Finding

Host `10.9.11.135` generated outbound network traffic that required
further investigation.

The suspicious activity was subsequently correlated using Zeek,
where DNS and TLS/SNI metadata provided additional evidence.

## Evidence

Wireshark screenshots from the initial packet analysis are included
in this directory.
