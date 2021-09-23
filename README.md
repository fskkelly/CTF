# Python現代密碼實測
2021/9/23

## pycryptodome
```
pip install pycryptodome
```

https://officeguide.cc/python-pycryptodome-aes-symmetric-encryption-tutorial-examples/

## libnum
```
pip install libnum
```
```
s2n(s) - packed string to number
n2s(n) - number to packed string
s2b(s) - packed string to binary string
b2s(b) - binary string to packed string
```
###example
```
import libnum

s="flag{happyCryptoDay}"
number=libnum.s2n(s)
number
```
```
print(libnum.n2s(number))
```
## gmpy2
1. 下載適合版本的gmpy2 https://www.lfd.uci.edu/~gohlke/pythonlibs/
2. 存到python安裝目錄的scripts
3. cmd中輸入wheel檢視是否已安裝
4. cd將目錄切換到scripts
5. pip install gmpy2檔名
