# Holistic Configuration Management at Facebook

### Note
1. Requirements
    * Configuration sprawl
    * Configuration authoring and version control
    * Defending against configuration erros
    * Configuration Dependency
    * Scalable and reliable configuration distribution
2. Architecture
    * Configuration authoring and version control
        * git:
            * share common configuration/lib as a repo
            * one project as one repo
            * seperate "configuration code" and "generated configuration file"
            * subscribe git change events/commit
    * Defending against configuration errors
        * universe configuration file format, make syntax verify easier
            * rfc:
                * json
                * yaml
                * ...
            * software integrated verify option
                * nginx -t
                * haproxy -c
                * ...
            * some common software configuration pidfall verify tools
                * secure configuration baseline
                * performance configuration baseline
                * ...
        * code/configration review
            * change as commit, commit as pull request
            * review requested before merge pull request into master
                * require dependency project maintainer to do code review ?
        * test
            * self test
            * A/B test
            * canary test
                * use api gateway to control "canary" traffic percentage
    * Configuration Dependency
        * build service/project Dependency Topology
            * to do MOC ("management of change")
    * Configuration distribution
        * mix with "push" and "pull" mode
        * large file only distribute metadata file
            * data file distribute via "p2p"
        * cache latest working version configuration file
    * Monitoring, alerts, and remediation
        * SLI monitor and alerts to identify error/performance impact
3. Tools
    * Configerator
    * Gatekeeper
    * PackageVessel
    * Sitevars
    * MobileConfig
4. Workflow
```
code/web -> push -> verify -> test -> identify dependency
-> code review -> (A/B|Canary) test -> apply configuration change
```

### Implementation
1. Tools
    * version conrol
        * git
    * api gateway
        * nginx/haproxy/envoy/kong
    * cache
        * nginx/rsync/squid/varnish
    * distribute
        * git hook
        * rsync hook
        * p2p
    * CI/CD
        * jekins/GoCD

### Reference
1. https://research.fb.com/wp-content/uploads/2016/11/holistic-configuration-management-at-facebook.pdf
