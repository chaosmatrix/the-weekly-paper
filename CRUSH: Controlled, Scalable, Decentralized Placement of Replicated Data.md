# CRUSH: Controlled, Scalable, Decentralized Placement of Replicated Data

## Implementation
1. ceph

## Note
1. Algorithm

|Action| Uniform|List|Tree|Straw|
|------|------|------|------|------|
|Speed|O(1)|O(n)|O(logn)|O(n)|
|Addditions|poor|optimal|good|optimal|
|Removals|poor|poor|poor|good|optimal|

## The Other Thought
1. Use less information get more information
    * algorithm
    * timestamp
    * move location
        * background
        * triggered by request
    * store information in key prefix
        * timestamp etc.

## References
1. https://ceph.com/wp-content/uploads/2016/08/weil-crush-sc06.pdf
2. https://ceph.com
3. mongodb Sharding
4. redis cluster

