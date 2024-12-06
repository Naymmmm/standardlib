---
description: Miscellaneous functions for executors.
---

# Executor

{% hint style="info" %}
This isn't really required, but it's nice to have for compatibility.
{% endhint %}

<pre class="language-lua"><code class="lang-lua"><strong>-- Import the executor library.
</strong><strong>local exe = require("@lib/executor")
</strong></code></pre>

## getexecutor()

This function returns the pascal-case version of the currently running executor.

```lua
-- Write a file.
exe.getexecutor()

-- Example
exe.getexecutor() -- May return Wave, SynapseZ, Xeno, or Unset if not declared.
```
