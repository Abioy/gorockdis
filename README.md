Wrap RocksDB inside a server talks like the REDIS.

For now, I am using tecbot/gorocksdb Go wrapper for RocksDB which needs his fork of RocksDB.

Dependencies:
* RocksDB: github.com/tecbot/rocksdb
* RocksDB Go Wrapper: github.com/tecbot/gorocksdb
* go get code.google.com/p/gcfg

Support commands:
* Keys: del, type, exists, keys
* Strings: getset, get, set, mget, mset, append, incr, incrby, decr, decrby
* Lists: lpush, rpush, lpop, rpop, lrange, lindex, llen

Config:
Please refer to rockdis.conf for example.
$ go run *.go -conf=rockdis.conf

Thanks for the idea and code from https://github.com/dotcloud/go-redis-server