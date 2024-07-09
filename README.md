# VSCode Example
## Import to require
1. Toggle into 'Find' window
2. Put the following regex
   Regex
   ```
   ^\s*import\s*(\{*\s*[A-Za-z0-9,\s]+\s*\}*){1}\s*from\s*(["']*[A-Za-z0-9/\-\.]+["']*){1}\s*;{0,1}\s*$
   ```
3. And replace with:
   Replace
   ```
   const $1 = require($2);
   ```
