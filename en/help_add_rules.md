## Add check byte expression
### Available Operator
|name | operator |
| ------- | ---------|
|+ - × ÷|+ - * /|
|AND|@&|
|OR|@&#124;|
|XOR|@^|
|NOT|@~|

### Example
rules → how to add  
`b2=b1` →`b2=b1`  
`b4=b2 + 0x1F` → `b4=b2+31`  
`b15=b0 xor b1` → `b15=b0@^b1`  
`b2=not b0` → `b2@~b0`  
*Note1: Please convert the hexadecimal number to decimal*  
    
### Extended Usage  
Visit [mXparser](http://mathparser.org/?s=Bitwise) WebSite