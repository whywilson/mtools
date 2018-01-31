# 教程1

## 要求：

1. 一部支持NFC的手机  
2. 知道IC卡的密钥ab  

（不知道的请下载M keys进行尝试破解）


## 步骤：

### 第一步(添加水卡)  
打开软件M Tools，点击加号，添加一张IC卡。
![Screenshot_2018-01-30-19-15-55-170_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a7103b22f09c.png)  
添加之后，点击详情，点击添加密钥，左边选择你金额扇区，比如我的是8扇区，如下图
![Screenshot_2018-01-30-19-23-06-446_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710458f172d.png)   

### 第二步(添加规则)  
点击扇区左边的按钮，选择需要更改的块
  
先标记金额，比如我的ic卡前三位是金额，所以标记下前三位，然后验证，选择倒置，倍率为100，点击下一步  
![Screenshot_2018-01-31-08-22-01-725_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710c7852d7b.png)  
### 第三步(标记校验字节)  
校验字节就是随你金额而变动的字节，只要会变动就都标记  
![Screenshot_2018-01-31-08-25-49-636_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710d1ad205d.png)  

标记完成后就填写下方表达式  
表达式也就是计算公式  

例如：
金额数据如下：

```
6D 20 00 00 FF FF FF FF 6D 20 00 00 20 DF 20 DF
```

比如我的b0,b1,b2(6D,20,00)是金额，同样b8 b9 b10也是金额，可以说是b8,b9,b10随b0,b1,b2改变而改变

表达式可以这样写：

```
b8=(b0)

b9=(b1)

b10=(b2)
```

![Screenshot_2018-01-31-08-25-24-308_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710dc39c5f5.png)

举例：
校验位算法 → 填写方式
```
b2=b1 →b2=b1
b4=b2+0x1F → b4=b2+31
b15=b0 xor b1 → b15=b0@^b1
b2=not b0 → b2@~b0
```
注1：请将十六进制数转换成十进制  
注2：按从上至下的顺序计算

写完后点击OK  
其它块如果相同，需重新添加或复制  

### 第四步(充值金额)  
卡片拿开重新放上，显示金额  
![Screenshot_2018-01-31-08-29-57-623_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710e18c0969.png)  
输入金额，点击＄按钮  
![Screenshot_2018-01-31-08-30-53-778_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710e52afa6c.png)  
![Screenshot_2018-01-31-08-30-58-352_tk.toolkeys.mtools.png](https://i.loli.net/2018/01/31/5a710e52ba734.png)  

*ps:如果出错请检查你的算法及表达式*



