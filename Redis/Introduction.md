# Redis Open Source

1. Redis is an in-memory data store used as a 
    - cache
    - vector database
    - document database
    - streaming engine
    - message broker
2. Has built-in replication and different levels of on-disk persistence.
3. supports complex data types (for example, strings, hashes, lists, sets, sorted sets, and JSON), with atomic operations defined on those data types.
4. There are different ways Redis can be installed, Please refer to [official documentation](https://redis.io/docs/latest/operate/oss_and_stack/install/install-stack/) for more details regarding installation, i will be currently using Ubuntu 22.04 (Jammy Jellyfish) kuberneties deployment.


## Redis Application
1. Caching and Session Management
2. Vector Search

## Basic Data Structure

1. GET, SET, UNLINK: For Strings
    - SET <key> <Value> -> Update Command
    - GET <key> -> Fetch Command
    - UNLINK <key> -> Delete Command

2. LPUSH, LLEN, RPOP, RPUSH, LPOP, LRANGE, LINDEX: For Lists
    - Used when order matters

3. SADD, SMEMBERS, SCARD, SREM: For Sets
    - Unordered, distict, 

4. HSET, HGET, HGETALL, : For hashes
    - Key Field Value
    - Other commands: Expire Fields, Store and increment numbers, Return random fields, remove fields,
    - Index and searching 

5. ZADD, ZSCORE, ZRANK, ZRANGE (withscores): Sorted Sets    
    - A set where each members is associated with a score.
    - Getting the count of a range
    - Lexical Sorting
    - Selecting Random members
    - Storing unions and intersections
    - Deleting members

6. JSON.SET, JSON.GET,JSON.DEL : For JSON

## Advance Data  Structure

1. Bitmaps
2. Bit Fields
3. Geospatial Indeces
4. Hyperlog-logs
5. Streams
6. Bloom Filters
7. Vectors
8. Timeseries
9. Probabilistic

## Use Key Expiration

1. Persistent: Stays until removed.
2. Volatile: Time to Live (TTL)
    - Expire <key> 30 -> in seconds
    - used in Session Management
    - EXPIREAT <key> 4481067600 -> UNIX Timestamp


