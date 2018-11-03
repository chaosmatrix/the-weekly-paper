# AutoScale: Dynamic, Robust Capacity Management for Multi-Tier Data Centers

### Note
1. when to shutdown server
    * base on load
2. how to shutdown server
    * SNMP/Agent
3. service require
    * stateless
    * support shutdown/start any time
4. how to define server load
    * qps
    * max/min/avg/variance request size
    * reserve capacity
5. Limititation
    * how to define server load
    * when to turn off/on system/server
    * server must stateless and can be shutdown/start at any time
6. Others
    * Data Center Design
        * location on low power price place
        * location on cold place
        * ...
    * Cloud or Container
    * Lower setup time
        * System Power Policy
        * Suspend System

### Implementation
1. Haproxy
    * https://github.com/haproxy/haproxy/blob/master/src/lb_fas.c

### Reference
1. http://reports-archive.adm.cs.cmu.edu/anon/2012/CMU-CS-12-109.pdf 

