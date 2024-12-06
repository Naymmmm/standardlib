---
description: Basic filesystem functions for basic filesystem needs.
---

# Filesystem

{% hint style="info" %}
Take caution when developing filesystem functions, these functions could cause catastrophic damage if you do not pay attention when developing.
{% endhint %}



<pre class="language-lua"><code class="lang-lua"><strong>-- Import the filesystem library.
</strong><strong>local fs = require("@lib/filesystem")
</strong></code></pre>

## writefile()

This function writes a file to the local filesystem, in a shared region.

```lua
-- Write a file.
fs.writefile(content: string, filename: string, location: string) -- Creates a new file if it doesn't exist, else it overrides.

-- Example
fs.writefile("These tacos are tasty, hawk tuah!", "what.txt", "./Yapping") -- Create a new folder if it doesn't exist.
```



## readfile()

{% hint style="warning" %}
This is a potentially dangerous function and could lead to security issues.
{% endhint %}

This function reads a file from the local filesystem, in the shared folder. It is important you do not expose your environment to foreign files and restrict it to a shared region.

```lua
-- Read a file.
fs.readfile(file: string): string

-- Example
fs.readfile("./Yapping/what.txt") -- Errors if it could not find the file.
```

## deletefile()

{% hint style="danger" %}
This is a dangerous function. Treat with caution.
{% endhint %}

This function deletes a file from the local filesystem, it is CRITICAL that you limit this function to the shared region and add safeguards to prevent operating system DESTRUCTION. Letting this function access foreign areas could cause CATASTROPHIC damage to the user.

```lua
-- DANGER: Deletes a file!
fs.deletefile(file: string): string

-- Example
fs.deletefile("./Yapping/what.txt") -- Errors if it could not find the file. Be careful when developing.
```
