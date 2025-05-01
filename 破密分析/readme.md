## 密碼學
- 古典密碼學
- 現代密碼:
  - 1970年代興起 ==> 以難解的數學問題當作安全依據 ==>會被量子電腦無情的摧殘 
  - 對稱金鑰加密 ==> DES(Data Encryption Standard，1976)
    - 區塊加密法
    - 串流加密法 
  - 公開金鑰加密 ==> RSA(1977)==> 數位簽章 ==> PKI
  - HAsh雜湊函數              ==> 數位簽章 ==> PKI
- 量子密碼(Quantum cryptography)
  - https://zh.wikipedia.org/zh-tw/%E9%87%8F%E5%AD%90%E5%AF%86%E7%A2%BC%E5%AD%B8 
  - 利用量子力學的特性來加密的科學。
  - 量子密碼學最著名的例子是量子金鑰分發 
- 後量子密碼(Post-Quantum Cryptography (PQC))
  - https://en.wikipedia.org/wiki/Post-quantum_cryptography
  - https://www.nist.gov/cybersecurity/what-post-quantum-cryptography 

## 古典密碼破秘分析
- 凱撒密碼(Caesar_cipher)
  - 頻率分析法 
- Vigenère cipher
- 密碼棒破密分析

#### 破密分析101:基礎題 CRY1
```
底下是加密過的密文(ciphertext) :

xyzqc{t3_qelrdeq_t3_k33a3a_lk3_lc_qe3p3}

你可以解密她嗎?

本題來自國外ABCTF的題目

凱撒密碼:維基百科
https://en.wikipedia.org/wiki/Caesar_cipher
https://zh.wikipedia.org/wiki/凱撒密碼

線上解題需特別注意有那些沒有被處理
你可以試試看看有沒不同
https://planetcalc.com/1434/
http://md5decrypt.net/en/Caesar/
https://www.xarg.org/tools/caesar-cipher/
```
#### 破密分析101:基礎題 CRY2  CRY2_凱撒密碼part2
```
解開底下秘文:

Pxevhfx mh tgzlmkhfvmy. Px ahix rhn xgchr hnk vmy. tvmy{utvd_mh_max_ynmnkx}.

線上解題需特別注意有那些沒有被處理
你可以試試看看有沒有不同
https://planetcalc.com/1434/
http://md5decrypt.net/en/Caesar/
https://www.xarg.org/tools/caesar-cipher/
```

#### 破密分析101:基礎題 CRY3_ROT13
```
ROT13的奧秘

OernxNYYPGS{kg_gvzr_V'yy_gel_2_ebha_ZNMldSDw}
```

#### 破密分析101:基礎題 CRY4_ SCYTCRYPTO 密碼棒破密
```
解開底下秘文:
Decrypt this strange word: ERTKSOOTCMCHYRAFYLIPL

本題目來自國外EKOPARTY CTF的題目

解答也就會有相關文字
```

#### 破密分析101:基礎題 CRY5_Vigenère cipher
```
Crack the cipher: vhixoieemksktorywzvhxzijqni

Your clue is:
"caesar is everything. But he took it to the next level."
```

- Vigenère cipher:https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher
- 參考看看: https://www.guballa.de/vigenere-solver

#### 破密分析101:基礎題 CRY6_頻率分析法
```
There's an authorization code for some Thyrin Labs information here,
along with someone's favorite song.
But it's been encrypted! Find the authorization code.
encrypted.txt

Hint:You may want to look at what the relative frequencies of letters in english text are.

底下網站有用:
http://quipqiup.com/
```
#### 破密分析101:基礎題 CRY7_Rail Fence Cipher
```

你會Rail Fence Cipher 籬笆式位移密碼嗎?

跟著Wiki學Rail fence cipher https://en.wikipedia.org/wiki/Rail_fence_cipher

解底下題目吧! 密文如下: Ta _7N6DE7hlg:W3D_H3C31N__BD4ef sHR053F38N43D47 i33___NC

使用四層籬笆(rail fence with 4 rails)

答案格式:BreakAllCTF{flag}

https://www.dcode.fr/rail-fence-cipher
```
#### 破密分析101:基礎題 CRY8_ROT47
```
你知道下列文字如何解密嗎？

qC62<p{{r%uL(92E0`D0#_%cfnm]kN

上網去GOOGLE ROT47

主動學習:請說明其原理
```
## 進階破密分析102:
#### 進階破密分析102:CRY11_PythonCrypto
```
錒錒去參加BREAKALLCTF 練習賽, 其中有一題密碼學的破密分析 讓她昏頭

你能教她如何解這題嗎?

密文(ciphertext)如下

cvqBeqacRtqazEigwiAobxrKobxrAobxrLwgk8Lwgk8CrtuiTzahfFreqc{bnjrZwgk8Ikgd4Pj85ePgb_e_rwqr7fvbmHjklo3tews_hmkogooyf0vbnk0ii87Drfgh_n kiwutfb0ghk9ro987k5tfb_hjiouo087ptfcv}
```
#### 進階破密分析102:CRY12_變形caesar密碼
```
有一題RC3 CTF的題目困擾小梅許久,你能幫她解出來嗎?

題目提示如下:
“The fault, dear Brutus, is not in our stars, but in ourselves.”
(I.ii.141) Julius Caesar in William Shakespeare’s Julius Caesar

密文(CipherText): 7sj-ighm-742q3w4t

請你解出明文!
```

#### 進階破密分析102:CRY13_affine-cipher
```
巅巅去參加國外CTF競賽,其中有一題讓她困擾不已. 你能幫她解出來嗎?

她只記得加密規則如下:
for each letter of cipher text its position in the alphabet is the position of the original letter multiplied by 4 and shifted by 15 character

shift over alphabet is cyclic, so 'z' shifted by 1 is _ and _ shifted by 1 is 'a'

aplhabet consists of letters from 'a' to 'z' and symbol '_'

letter 'a' has position 0, symbol '_' has position 26 (following 'z')

密文如下: ifpmluglesecdlqp_rclfrseljpkq

請你解出明文吧!
```
#### 進階破密分析102:CRY14_加密的奧義
```
阿義去參加CTF競賽,有一題困擾他許久,你能完成底下加密方法嗎?

加密方法:
將每個數字 mod 37後所得到的答案依序轉成對應的字母:
0-25 對應到大寫的英文字母(0是A, 1是B,...依此類推),
26-35對應到0-9數字,
36 對應到底線('_').

數字: 91 322 57 114 40 406 272 147 239 285 353 272 77 110 296 262 299 323 255 337 150 102

請問數字破密後得到的明文為何?
答案格式:BreakallCTF{加密後的答案}
```






