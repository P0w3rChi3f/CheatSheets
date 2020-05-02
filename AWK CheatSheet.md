# AWK  

Tool Usage and Syntax  

* awk [options] [/pattern/] [{action}] [file]  
* -F = delimiter
* / / = pattern (regex)
* { }= action
* ! = not
* -f = read file

Examples  

* awk -F, '{print "Name=" $1 " State=" $2}' presidents.csv  
* awk -F, '/x/ {print "Name=" $1 " State=" $2}' presidents.csv
* awk -F, 'BEGIN {print "Name      State"} {print $1,$2}' presidents.csv
* awk -F, END {print "Name      State"} {print $1,$2}' presidents.csv
* awk -F ',' '{ print $ }' presidents.csv | sort | awk -f states.awk
