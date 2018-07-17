Keccak in Python
================
This is Keccak.py implementation. To get the same output as keccak1600() in monero's slow_hash, the squeezing part if omitted.
It is Keccak-256 (with b=1600, c=512, r=1088) and "output" of 1600 bits). The input to slow_hash during pool mining will be blob of 152 chars (hex encoded 76 bytes).
To run (`s` is the input in hex digits, `True` is for debug state after each round):
```
$ python
>>> s='aabbcc'
>>> import Keccak
>>> myKeccak=Keccak.Keccak()
>>> myKeccak.Keccak((len(s)*4,s),1088,512,1600,True)
```

Original MiniNero README below...

MiniNero
========

This repository contains code used to prototype research for the cryptocurrency Monero. Also, there will occasionally be some drafts of math research related to various experimental extensions of the protocol. This written up research is hashed into the blockchain for timestamping purposes. 

For current Ring CT code in python, I have separated this out in the following repository: 

https://github.com/ShenNoether/RingCT-Python

For current Ring CT code in c++, I have refactored this in the following repository: 

https://github.com/ShenNoether/RingCT 

#Note:
MiniNero is also the name for the suite of mobile monero wallets with [xmr.to](https://xmr.to/) integration. 

[MiniNero Web: React-based web-wallet and NodeJS server](https://github.com/shennoether/mininodo)

[MiniNero Universal: Windows 10 Mobile Wallet in C#](https://github.com/shennoether/MiniNeroUniversal)

[MiniNero Droid: Android Mobile Wallet in Java](https://github.com/shennoether/MiniNeroDroid)

The name "MiniNero" is chosen because these apps aim to provide a light-weight, easy-to-use Monero experience.  
