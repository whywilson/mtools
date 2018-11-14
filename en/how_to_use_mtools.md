# How to use MTools
Firstly, it's an APP that I used to write hex datas back to mifare 1k card with my NFC phone - Moto X 2013. And after several steps of studies and development, I find a way to read the money data from card and generate legal hex data then write back it to the card. And it works perfectly, which made me so happy. Seemed like I'm a dark hacker, can easily change the money on the card with a simple app.
After that I want to share this happiness to all guys who are interested in RFID. After about 3 weeks development the first version of MTools came out.
Here're the things that you need to know to use it better.

- Get the keys from all sectors
- Compare to find the sector with money data
- Add card, sector and  keys to MTools
- Record data from after every consumption in sniffer
- Compare and analyze the rules of dynamic bytes
- Finish the expression
- Charge mifare 1k  card with one click

---

## Get the keys from all sectors

Some cards using default keys like `FFFFFFFFFFFF` `000000000000` `A1B2C3D4E56F` etc, which you can try to dump keys with **Mifare Classic Tools** on the NFC android phone. 
If the card is not full encrypted, it can be cracked with RFID device to burst crack. Like **ACR122U** or **PN532**.

If the card is full encrypted,  only **PM3** can crack the keys.

## Compare to find the sector with money data

With keyA or keyB of all sectors of card, datas need to be gathered. And compare them after every consumption, so you can find the sector that datas change, which means the money data may in that sector.

## Add card, sector and  keys to MTools

The 4th block of every sector contains 

`keyA(6 bytes) +  Access Control(4) + keyB(6)`

## Record data from in sniffer

With sector number and valid keys added, it can be easy to compare data with different money amount.

Mark the money bytes(contain money data) and check bytes(mostly the changing bytes)

## Compare and analyze the rules of dynamic bytes

Pay attentions on HEX or DEC, Reverse or not and Rate on Money bytes.

Compare the Summation or XOR values with up and down check bytes.

## Finish the expression
MTools use [mXparser](http://mathparser.org/) to calculate expression in rules. Please follow the tips in MTools to add expression.
## Charge mifare 1k  card with one click
Before Charge card, an accurate simulation is necessary, just by long click on the $ button after tag card.
 ## One more thing
MTools support work with extra device like ACR122U, which means you can use a phone without NFC hardware.