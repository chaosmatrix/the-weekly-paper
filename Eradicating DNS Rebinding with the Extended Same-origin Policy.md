# Eradicating DNS Rebinding with the Extended Same-origin Policy

## Note
1. DNS Pining
    * browser: keep domain and ip cache  until browser close
    * browser: implement min TTL force, aka 60s
    * dns cache server: implement min TTL force, aka 60s
2. SOP and eSOP
3. RFC1918: restrict private address
    * whitelist
4. Gateway Firewall Monitor
    * protocol base anylazy
    * protocol port monitor
5. Internal Server
    * Auth require
        * Username and Password Auth Required
        * Host Name Authorization, relies on reverse DNS
    * Host filter

## Implemation
1. Browser: restric protocol and protocol service base port
    * aka. not allow send http request to port 21/22/23...

## References
1. https://www.usenix.org/system/files/conference/usenixsecurity13/sec13-paper_johns.pdf
2. https://www.w3.org/Security/wiki/Same_Origin_Policy
