# Consistent Hashing with Bounded Loads

### Implementation
1. Nginx
    * upstream chash, both http and stream
2. Haproxy
    * hash-balance-factor
    * via forwarding, respecting server load

