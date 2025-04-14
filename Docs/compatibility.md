---
description: Miscellaneous functions to ensure compatibility.
---

# Compatibility



{% hint style="info" %}
These functions are to maximize compatibility.
{% endhint %}

```lua
-- Import the executor library.
local comp = require("@lib/compatibility")
```

## unc(sunc: bool?)

Runs a UNC, sUNC if provided. This is mainly for compatibility reasons and testing, you do not need to implement this.

```lua
-- Example
comp.unc(true) -- Starts an sUNC test
comp.unc() -- Starts a regular UNC test
```
