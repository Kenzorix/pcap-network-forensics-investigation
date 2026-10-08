# Activity Timeline
## Suspicious Activity Window
Network activity associated with the identified suspicious domains was observed from approximately:

**20:06:33 UTC → 20:19:08 UTC**

Duration: **~12 minutes 36 seconds**

## Timeline

| Time | Event |
|---|---|
| 20:06:33 | TLS connection to `winrun2915.com` |
| During investigation | Repeated DNS queries for identified suspicious domains |
| During investigation | Repeated TLS/HTTPS connections to the identified infrastructure |
| 20:19:08 | Last observed matching TLS connection to `logincrypt8338.com` |

## Assessment

The timeline shows repeated outbound communication from `10.9.11.135` with the identified suspicious infrastructure during the observed activity window.

The timeline establishes network activity but does not by itself establish execution or persistence on the endpoint.
