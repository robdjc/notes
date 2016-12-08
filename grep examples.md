A collection of grep commands for supporting trading applications.

Return everything in the file and just highlight the matching pattern:

`grep  --color=auto -E "ERR|" application.log`

Get a substring between two delimiters from a line.

`grep -o -P '(?<=\[).*(?=\])'
