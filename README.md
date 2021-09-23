# Python現代密碼實測
2021/9/23

## pycryptodome
```
pip install pycryptodome
```

### AES加密
```
from Crypto.Cipher import AES
from Crypto.Random import get_random_bytes

data =b'falg(HappyCryptoDay)'
key = get_random_bytes(16)
cipher = AES.new(key, AES.MODE_EAX)
ciphertext, tag = cipher.encrypt_and_digest(data)

file_out = open("encrypted.bin", "wb")
[ file_out.write(x) for x in (cipher.nonce, tag, ciphertext) ]
file_out.close()
```

### AES解密
```
from Crypto.Cipher import AES

file_in = open("encrypted.bin", "rb")
nonce, tag, ciphertext = [ file_in.read(x) for x in (16, 16, -1) ]

# let's assume that the key is somehow available again
cipher = AES.new(key, AES.MODE_EAX, nonce)
data = cipher.decrypt_and_verify(ciphertext, tag)
```

## libnum
```
pip install libnum
```

## gmpy2
1. 下載適合版本的gmpy2 https://www.lfd.uci.edu/~gohlke/pythonlibs/
2. 存到python安裝目錄的scripts
3. cmd中輸入wheel檢視是否已安裝
4. cd將目錄切換到scripts
5. pip install gmpy2檔名
