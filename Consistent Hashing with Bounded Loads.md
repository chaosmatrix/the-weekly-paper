# Consistent Hashing with Bounded Loads

### Implementation
1. Nginx
    * upstream chash, both http and stream
2. Haproxy
    * hash-balance-factor
    * via forwarding, respecting server load

### Reference
1. https://arxiv.org/abs/1608.01350
2. Maglev: A Fast and Reliable Software Network Load Balancer

