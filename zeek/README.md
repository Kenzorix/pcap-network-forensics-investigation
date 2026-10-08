# Zeek Analysis
## Objective

Zeek was used to extract and analyze network metadata from the PCAP,
with a focus on DNS and TLS activity.

## DNS Analysis
Repeated DNS queries were observed from host `10.9.11.135` for the
following domains:

- `winrun2915.com`
- `logincrypt8338.com`
- `opscast3707.net`

The DNS responses were correlated with the destination IP addresses
observed in the traffic.

## TLS Analysis

Zeek `ssl.log` showed repeated TLS connections from `10.9.11.135`
to the suspicious domains over TCP port `443`.

The observed TLS activity included:

- `winrun2915.com`
- `logincrypt8338.com`
- `opscast3707.net`

## Activity Window

The suspicious TLS activity was observed approximately between:

**20:06:33 and 20:19:08 UTC**

This represents approximately **12 minutes and 36 seconds** of
observed activity.

## Assessment

The DNS and TLS evidence indicates suspicious outbound communication
from `10.9.11.135`.

The network evidence alone does not prove malware execution or
persistence on the host.
## Evidence

Relevant Zeek DNS, TLS/SNI, correlation, and timeline screenshots are
included in this directory.
