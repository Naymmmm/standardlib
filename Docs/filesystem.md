# Filesystem



<pre class="language-lua"><code class="lang-lua"><strong>-- Import the filesystem library.
</strong><strong>local fs = require("@lib/filesystem")
</strong></code></pre>

## writefile()

This function writes a file to the local filesystem, in a shared region.

```lua
-- Write a file.
fs.writefile(content: string, filename: string, location: string)

-- Example
fs.writefile("These tacos are tasty, hawk tuah!", "what.txt", "./Yapping") -- Create a new folder if it doesn't exist.
```



## readfile()

This function reads a file from the local filesystem, in the shared folder. It is important you do not expose your environment to foreign files and restrict it to a shared region.

```lua
-- Read a file.
fs.readfile(file: string): string

-- Example
fs.readfile("./Yapping/what.txt") -- Errors if it could not find the file.
```
