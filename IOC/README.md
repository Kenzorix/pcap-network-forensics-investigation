# Indicators of Compromise (IOCs)
## Overview

The following indicators were identified during the network traffic investigation.

## IOC Table

| Type | Indicator | Observation |
|---|---|---|
| Internal Host | `10.9.11.135` | Source host generating the suspicious outbound traffic |
| Domain | `winrun2915.com` | Observed in DNS and TLS/SNI traffic |
| Domain | `logincrypt8338.com` | Observed in DNS and TLS/SNI traffic |
| Domain | `opscast3707.net` | Observed in DNS and TLS/SNI traffic |
| IP | `104.21.91.138` | Resolved infrastructure for `winrun2915.com` |
| IP | `172.67.221.70` | Resolved infrastructure for `winrun2915.com` |
| IP | `172.67.214.168` | Resolved infrastructure for `logincrypt8338.com` |
| IP | `104.21.42.254` | Resolved infrastructure for `logincrypt8338.com` |
| IP | `172.67.180.55` | Resolved infrastructure for `opscast3707.net` |
| IP | `104.21.43.143` | Resolved infrastructure for `opscast3707.net` |

## Assessment

The domains were treated as the primary suspicious network indicators because they were repeatedly observed in DNS and TLS/SNI activity.

The associated IP addresses are documented as observed infrastructure and should not be considered malicious solely based on their appearance in the PCAP, particularly where shared hosting or CDN infrastructure may be involved.

## Recommended SOC Actions

- Search the identified domains across DNS and proxy logs.
- Check endpoint telemetry for connections to the identified infrastructure.
- Enrich the indicators with current threat intelligence.
- Investigate the affected host `10.9.11.135` for evidence of execution or persistence.
- Monitor for future connections to the identified domains.
