# MITRE ATT&CK Mapping
## Overview

The observed network behaviors were mapped to MITRE ATT&CK techniques
based on the available PCAP evidence.

Only techniques supported by the evidence were included.

## Technique Mapping

| Technique | ID | Evidence |
|---|---|---|
| Application Layer Protocol: Web Protocols | T1071.001 | Repeated TLS/HTTPS communication to suspicious domains |
| Application Layer Protocol: DNS | T1071.004 | Repeated DNS queries and resolutions for suspicious domains |

## Techniques Not Mapped

### T1105 — Ingress Tool Transfer

Not mapped because the PCAP did not provide sufficient evidence of
payload or file transfer.

### T1059.001 — PowerShell

Not mapped because no PowerShell execution evidence was identified.

### T1573 — Encrypted Channel

TLS encryption was observed, but the available evidence was not
sufficient to establish malicious use of encryption for command and
control. Therefore, it was not treated as a confirmed technique.

## Assessment

The mapping is intentionally limited to behaviors directly supported
by the network evidence. Additional endpoint telemetry could support
further ATT&CK mappings if available.
