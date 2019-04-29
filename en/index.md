[Select Language](../index.html)  

# 1.Overview
Here is a Material Design APP to make charge `Mifare Classic Card` easily.    
Attention:  

1. `Mifare 1K `Supported Device.  
(Or OTG support `ACR122U`)
2. KeyA and keyB of useful sector. 
3. Comply with local laws, only used for study and testing.

# 2.Tutorial  
[How to use MTools](./how_to_use_mtools.html)  
---  

### [YouTube](https://www.youtube.com/channel/UC5ZyMTY35t5G4BsmTfjWU9g)

- [Use MTools to read/write/clone datas on Mi Band 3 NFC](https://youtu.be/1Bl-FFALNic)
- [Hack Mifare 1K Card without ACR122U only MTools](https://youtu.be/hEwhJWAt3a8)
- [Burst Attack Mifare 1K Card with MKeys on NFC Android Phone](https://youtu.be/CKSBDwRg7Wo)

## 2.1 Lists
### 2.1.1 Add Card
Click the **+ floating button** will display `Add Card Dialog`, put the Mifare Classic Card close to the NFC antenna, then you can add a card to the APP.
### 2.1.2 Remove Card
Slide the item toward right to remove the card.
### 2.1.3 Sort Card
Press and drag to sort Cards.
## 2.2 Details
### 2.2.0 Interface Introduction  
![image](img/button_func.jpeg)
### 2.2.1 Add Key
Click the ** + floating button ** to display `Add Key Dialog`, select the sector number by sliding the picker, and enter 6 bytes (12 digits or letters) valid key A or key B, click ` Complete ` to save.
### 2.2.2 Modify Key
Click the ** modify button ** will display the `Modify Key Dialog`,  select new  sector number by sliding the picker, and modify the 6 bytes (12 digits or letters) valid key A or key B, click ` Complete `save new keys or sector.
### 2.2.3 Read Sector
After the card is close to the NFC antenna, click on the ** read button ** will read 4 block of data from clicked sector, you could modify and write the new data.  
### 2.2.4 Data Sniff/Compare
Must add correct keys before. After marked, it can be  compared with highlight datas.  
[Pro Version] Data Backups/Restore, Compare vertically, Rule Repository.  
### 2.2.5 Add Rule 
### 2.2.5.0 Interface Introduction   
Click data item to add/modify rule.  
Click icon to copy rule to another block of another sector.  
[Pro Version] Rule copy.
![image](img/select_block.jpeg)
#### 2.2.5.1 Add Money Byte
Mark the byte, then verify the money is correct, and click Next.  
![image](img/mark_money.jpeg). 
#### 2.2.5.2 Add Checked Byte    
Check the bytes that changes and add expressions. Make sure that it's correct then click OK.  
![image](img/mark_check.jpeg)
##### 2.2.5.2.1 Supported operations:
> And: +  
>
> Subtraction: -  
>
> Multiply: *  
>
> division: /  
>
> xor: @^  
>
> not: @~  
>
> Crc8:  crc8, crc8cdma2000, crc8darc, crc8dvbs2, crc8ebu, crc8icode, crc8itu, crc8maxim, crc8rohc, crc8wcdma  
>
> Crc16: crc16ccittfalse, crc16arc, crc16buypass, crc16cdma2000, crc16dds110, crc16dectr, crc16dectx, crc16dnp, crc16en13757, crc16genibus, crc16maxim, crc16mcrf4xx, crc16riello, crc16t10dif, crc16teledisk, crc16tms37157, crc16usb, crca, crc16kermit, crc16modbus, crc16x25, crc16xmodem    

*Note1: Only decimal arithmetic is supported*    

*Note2: Crc expression must be called as shown above*    

**Get Expressions Example [Click Here](./help_add_rules.html)**  

##### 2.2.5.2.2 Sort Expressions 
Press and drag to sort Expressions.   

The calculation is from top to the end.

### 2.2.6 Sort Keys
Press and drag to sort Keys.
###	2.2.7 Remove Key
Slide the item toward right to remove the key.
### 2.2.8 key Lists 
Long press the floating button to show key lists.  
## 2.3 Charge
### 2.3.1 Set Quotas
Long press **the Charge TextView** , you can charge as the Quotas. 
### 2.3.2 Clear Record
Long press **the recharge record list**, then pop up the dialog will allow you to to clear the recharge record or not.  
### 2.3.3 Show Calculate Result 
Long press the floating button to preview the data generated on **Rule**.

# 3.Dependency  
Thanks for the friends on the contribution of open source community, regardless of rank.  
- `ikarus23` [MifareClassicTool](https://github.com/ikarus23/MifareClassicTool "MifareClassicTool")  
- `afollestad` [material-dialogs](https://github.com/afollestad/material-dialogs "material-dialogs")  
- `markormesher` [android-fab](https://github.com/markormesher/android-fab)  
- `didikee` [AndroidDonate](https://github.com/didikee/AndroidDonate "AndroidDonate")  
- `Ice-Box` [Ice-Box](http://catchingnow.com)  



<a href="https://www.vultr.com/?ref=7136930"><img src="https://www.vultr.com/media/banner_2.png" width="468" height="60"></a>