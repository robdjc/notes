# FIX Protocol
Command line examples for working with FIX Protocol log files.

######Remove SOH and make a message more readable

Using sed:
`grep something fix.log | sed 's/\x01/ | /g'`

Using tr:
`grep something fix.log | tr '\001' '|'`

Use grep to get a single FIX field:
`grep "35=D" fix.log | grep -o -w "55=[^[:cntrl:]]\+" | sort | uniq -c`

Grep command to return everything in the file and just highlight the matching pattern:
`grep  --color=auto -E "ERR|" application.log`
