环境：Python2

问题：
```python
m=(pow(c1,s1,n)*pow(c2,s2,n)) % n
hex(m)
print binascii.a2b_hex(m)
```
此时一直报错，错误信息为：

```
print binascii.a2b_hex(m)
TypeError: Odd-length string
```
黑人问号？

`print m`试了一下，发现`hex(m)`是这样的：

`0x666c61672d3534643364623563316566636437616661353739633337626362353630616530L`

多了`0x`和`L`

赶紧把这些碍事的家伙去掉。

`m=hex(m).replace('l','').replace('L','').replace('0x','')`

flag成功输出
