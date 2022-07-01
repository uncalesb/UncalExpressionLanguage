# UncalExpressionLanguage (U{E}L)

is a variabel-a-like used on a field of **UncalESB 1.1** to customize an input text value.\
the expression consists of **String** and **ExpressionLanguage**.\
**String** is a constant value that defined by user on input text as is.\
**ExpressionLanguage** is a predefined value that defined by UncalEngine at runtime, with notation **{$EL}**\
the expressions are:\
`$Counter()` = is a counter based on integration scenario with default digit is 5 and starts from 1\
`$DATE(_parameter_)` = is a current date with default format is **ddMMyy**\
`$TIME(_parameter_)` = is a current time with default format is **HHmmss**\
`$TIMESTAMP()` = is a current **yyy-MM-dd HH:mm:ss.SS**\
`$MILLIS()` = is a current time millisecond\
`$NANOTIME()` = is a current nanotime more unique than Millisecond\
`$ASIS()` = is same as source filename\
### File Name Content Parse (FNCP)
#### `$FNCP([*file_extension*],B*n*M*n*A*n*P=[*parameter*])`\
how to use:
`$FNCP(*.*,B1M0A10P=Jojot)` mean : find all file type, dive into file content, B1 = at line 1 M0 = from char index 0 to A10 = to char index 10 P=Jojot find word 'Jojot'\
`$FNCP(*.*,P=Jojot)` or `$FNCP(*.*,BSP=Jojot)` mean find all file type, dive into file content and file 'Jojot' in it. BS mean whole line of file content\
## for customization:
`$Counter(xxxxxx)` defined for 6 digit counter starts from 1\
`$Counter(00010)` defined for 5 digit counter starts from 11 (10 + 1)\
`$DATE(ddMMyyyy)` defined for 4 digit year\
`$TIME(mmss)` defined for minute and second only

## usage :
`String{$EL}String`\
e.g.\
`MFG_{$Counter}.txt`\
result :\
`MFG_00001.txt`
