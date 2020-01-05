## 添加校验字表达式
### 可用运算符
|名称 | 运算符 | 简化 |
| :-----: | --------- | ---------|
|+ - × ÷|+ - * /| |
|括号|( )| |
|与|@&| and |
|或|@&#124;| or |
|异或|@^| xor |
|取反|@~| not |
|连续求和|b1+b2+···+b14|sum(1:14)|
|连续异或|b1 xor b2 xor ··· xor b10|xor(1:10)|
|连续逻辑与|b1 and b2 and ··· and b14|and(1:14)|
|CRC8/CRC16|[参考此处](https://why.yuyeye.cc/post/how-to-calculate-crc8-and-crc16-in-mtools/)|[详细介绍](https://why.yuyeye.cc/post/how-to-calculate-crc8-and-crc16-in-mtools/)|

### 举例
`b2等于b1` →`b2=b1` 

`b4=b2加上0x1F` → `b4=b2+31` 

`b15=b0异或b1` → `b15=b0 xor b1` 

`b2=b0取反` → `b2=not b0`  

### 注意
- 请将十六进制数转换成十进制
- 上下拖动可更改计算顺序

### 拓展用法  
见 [mXparser](http://mathparser.org/?s=Bitwise) 官网
