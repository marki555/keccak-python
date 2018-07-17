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

Example inputs/outputs:
```
In :37a636d7dafdf259b7287eddca2f58099e98619d2f99bdb8969d7b14498102cc065201c8be90bd777323f449848b215d2977c92c4c1c2da36ab46b2e389689ed97c18fec08cd3b03235c5e4c62a37ad88c7b67932495a71090e85dd4020a9300
Out:9c715ff5defdb7ad24bf6055d077f58d0eebb84c8ef901dc6469f70d0119ce53aea1bc2733e147b3c263a0ee69f9856926aabd68cbf052b6014326c610f7f4b6602342412f0921952a5e27a5ff27c9ce0cd6f5102cec3979549d5f47a69385b29f0299b09e8f5e88eaa26506d08942009bedeecaa950205a634e4538c5fe33ee28b783552349e2df202c1784b517e35915c8bfaab6eb8d8ffb924bca634a1bcc2f5eae869f4e5307751933b91707cba1808414a2b247ad4403c9a95b93d85d8fd48f3f67f2f2cd36

In :38274c97c45a172cfc97679870422e3a1ab0784960c60514d816271415c306ee3a3ed1a77e31f6a885c3cb
Out:49f6704f216286b429c6ceed01580c2f1715acb1f9590c1f1ac582c58110e3915f63b4db1f7174bbf7ccf7ff8a6be8ca7a9bb5a4e6622b9ebeb0606834efbc280e705c2677cb34c87900c76d8120606ddc337f9ff6928b1e6c8f99570382b7901612c2dfd9493a07e10dd3e17e24a15cc2bf160b48d9a415417871210b7f402cdd3adb14e97a175bec4b7261cac27f79012861f6aa2fd6b85628d5f327711a94929da52490dbddb99e3e1c946adf9404fc27b8b9c0062286b2624e51f384a85f2bdd5d87d2dc4e52
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
