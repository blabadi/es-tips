# elasticsearch-tips

## Shards
- Aim to keep the average shard size between a few GB and a few tens of GB. For use cases with time-based data, it is common to see shards in the 20GB to 40GB range.
- Avoid the gazillion shards problem. The number of shards a node can hold is proportional to the available heap space. As a general rule, the number of shards per GB of heap space should be less than 20.
https://www.elastic.co/guide/en/elasticsearch/reference/current/scalability.html

## Storage
- master nodes should have persistent storage https://engineering.vulcan.com/2019_0128_Elasticsearch-on-Kubernetes.aspx
