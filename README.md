# 線上工具 == > 質因數分解
http://factordb.com/

# pycrypto
```
!pip install pycrypto
```

# pycryptodome
```
!pip install pycryptodome
```

# libnum
```
!pip install libnum
```
```
s2n(s) - packed string to number
n2s(n) - number to packed string
s2b(s) - packed string to binary string
b2s(b) - binary string to packed string
```
## example
```
import libnum

s="flag{happyCryptoDay}"
number=libnum.s2n(s)
number
```
```
print(libnum.n2s(number))
```
# gmpy2
```
!apt install libgmp-dev
!apt install libpfr-dev
!apt install libmpc-dev
!pip install gmpy2
```

1. 下載適合版本的gmpy2 https://www.lfd.uci.edu/~gohlke/pythonlibs/
2. 存到python安裝目錄的scripts
3. cmd中輸入wheel檢視是否已安裝
4. cd將目錄切換到scripts
5. pip install gmpy2檔名

# sympy
```
!pip install sympy
```
