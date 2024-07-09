# VSCode Example from ECMAScript to CommonJS
## Import to require
1. Toggle into 'Find' window
2. Put the following regex
   Regex
   ```
   ^\s*import\s*(\{*\n*\s*[A-Za-z0-9,_\s\n]+\s*\}*){1}\s*from\s*(["']*[A-Za-z0-9/\-\._]+["']*){1}\s*;{0,1}\s*
   ```
3. And replace with:
   Replace
   ```
   const $1 = require($2);
   ```
## Complex import
1. Toggle into 'Find' window
2. Put the following regex
   Regex
   ```
   ^\s*import\s*(\w+)\s*,\s*(\{+\s*[A-Za-z0-9,\s]+\s*\}+){1}\s*from\s*(["']*[A-Za-z0-9/\-\._]+["']*){1}\s*;{0,1}\s*$
   ```
3. And replace with:
   Replace
   ```
   const $1 = require($3);
   const $2 = $1;
   ```
## Export
1. Toggle into 'Find' window
2. Put the following regex
   Regex
   ```
   ^\s*export\s*default\s*([a-zA-Z0-9]*)\s*;*$
   ```
3. And replace with:
   Replace
   ```
   module.exports = $1;
   ```
