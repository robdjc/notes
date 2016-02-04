# FIX Protocol
Command line examples for working with FIX Protocol log files.



Examples to remove the SOH character and make FIX messages more readable. 

Using sed:

`grep something fix.log | sed 's/\x01/ | /g'`

Using tr:

`grep something fix.log | tr '\001' '|'`


Examples to work with the SOH character.

Use grep to get a single FIX field:

`grep "35=D" fix.log | grep -o -w "55=[^[:cntrl:]]\+" | sort | uniq -c`

Grep for a specific field. Sometimes you want to grep for Tag 39 only, but it matches other tags such as 139. The SOH can be used to only target Tag 39. Replace 39 with any other FIX Tag.

`grep -P "\x0139=1\x01" fix.log`

