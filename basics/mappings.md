---
description: ~dictionaries
---

# Mappings

Other than structs and arrays, its another way to store organized data in Solidity.

Defining a mapping looks like this:

```solidity
mapping (address => uint) public accountBalance;

mapping (uint => string) userIdToName;
```

Its essentially a key-value store for storing and looking up data.
