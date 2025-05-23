---
title: TTL
description: TTL returns the remaining time to live in seconds
---

<!-- This file is automatically generated. Any modifications made directly to this file
  may be overwritten. For more details on how this file is generated and how to use
  the related commands, refer to the documentation available in the `internal/cmd/cmd_*.go` files.
-->

#### Syntax

```
TTL key
```


TTL returns the remaining time to live (in seconds) of a key that has an expiration set.

- Returns -1 if the key has no expiration.
- Returns -2 if the key does not exist.
	

#### Examples

```

localhost:7379> SET k 43
OK
localhost:7379> TTL k
OK -1
localhost:7379> SET k 43 EX 10
OK
localhost:7379> TTL k
OK 8
localhost:7379> TTL kn
OK -2
	
```
