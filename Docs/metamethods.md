---
description: Metamethod related functions for overriding hooks or functions
---

# Metamethods



{% hint style="info" %}
These functions are to hook to external methods or functions and override meta tables.
{% endhint %}

```lua
-- Import the metamethod library.
local meta = require("@lib/metamethods")
```

## getrawmetatable(object: object): table

Same API as UNC. TBD

```lua
-- Example
meta.getrawmetatable(game)
```
