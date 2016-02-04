# FIX Protocol
Command line examples for working with FIX Protocol log files.



Examples to remove the SOH character and make FIX messages more readable. 

Using sed:

`grep something fix.log | sed 's/\x01/ | /g'`

Using tr:

`grep something fix.log | tr '\001' '|'`

Use grep to get a single FIX field:

`grep "35=D" fix.log | grep -o -w "55=[^[:cntrl:]]\+" | sort | uniq -c`


