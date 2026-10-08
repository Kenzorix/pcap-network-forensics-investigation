# PCAP Network Forensics Investigation
## Overview
This repository documents a network forensics investigation of a PCAP file, focusing on suspicious DNS and TLS/HTTPS activity, IOC identification, timeline reconstruction, and detection coverage.

I used Wireshark, Zeek, and Snort to investigate suspicious network
traffic, identify IOCs, build a timeline, and map the observed
activity to MITRE ATT&CK.

## What I Investigated

- DNS queries
- TLS/HTTPS connections
- Suspicious domains
- Source and destination IPs
- Network activity timeline
- IDS detection coverage

## Main Finding

Host `10.9.11.135` made repeated DNS and TLS connections to:

- `winrun2915.com`
- `logincrypt8338.com`
- `opscast3707.net`

The traffic was suspicious, but the PCAP alone did not prove that
malware was executed on the host.

Further endpoint investigation would be required.

## Tools

- Wireshark
- Zeek
- Snort
- MITRE ATT&CK
- Ubuntu

## MITRE ATT&CK
| Technique | ID | Reason |
|---|---|---|
| Web Protocols | T1071.001 | TLS/HTTPS communication was observed |
| DNS | T1071.004 | DNS queries to suspicious domains were observed |

I only mapped techniques that were supported by the network evidence.

## Detection Gap
Zeek showed suspicious DNS/TLS activity, but I did not confirm a
matching Snort alert from the output examined.

This may indicate a detection coverage gap and should be investigated
further.

## Conclusion
The PCAP shows suspicious outbound communication from 10.9.11.135 to the identified infrastructure. The available network evidence supports further investigation but does not independently establish malware execution or persistence. the next step would be endpoint investigation and correlation with host-based telemetry.
