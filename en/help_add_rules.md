## Add check byte expression
### Available Operator
|Name | Operaor | Simple |
| :-----: | --------- | ---------|
|+ - × ÷|+ - * /| |
|brackets|( )| |
|and|@&|  |
|or|@&#124;|  |
|xor|@^|  |
|not|@~|  |
|Continuous summation|b1+b2+···+b14|sum(1:14)|
|Continuous XOR|b1 xor b2 xor ··· xor b10|sum(1:10)|
|Continuous logical AND|b1 and b2 and ··· and b14|and(1:14)|
|CRC8/CRC16|[Know more](https://why.yuyeye.cc/post/how-to-calculate-crc8-and-crc16-in-mtools/)|[Know more](https://why.yuyeye.cc/post/how-to-calculate-crc8-and-crc16-in-mtools/)|


### Example
rules → how to add 
`b2=b1` →`b2=b1` 
`b4=b2 + 0x1F` → `b4=b2+31`
`b15=b0 xor b1` → `b15=b0@^b1`
`b2=not b0` → `b2@~b0` 
*Note1: Please convert the hexadecimal number to decimal* 
*Note2: Drag expression up/down to change sequence*
    

### Extended Usage  
Visit [mXparser](http://mathparser.org/?s=Bitwise) WebSite
