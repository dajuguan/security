- policy： pemmission, password
    - Insecure defaults
- threat model
    - secret design/impl: 设计泄露后需要完全重新设计，更好的是通过秘钥，即使泄露可以更换
    - assmuming specific attack vectors: captcha(验证码)解题困难，设置rate limit =>攻击者找到便宜人工来识别这些来绕过 
    - certificate authorities: 最开始设计有很少CA可信任没问题，但拓展到有很多CA机构时失效了，找到最弱的compromised来入侵
    - software dev:
        - source repo. git
        - source dev tool => xcode修改攻击
        - software update
- mechanism(bugs): os, crypo device
    - bugs in software
    - bugs in policy impl:
        - apple iCloud rate limit login attempts: 很多api中有一个api忘记设置了
        - software require many checks很容易出错
    - randomness for crypto:伪随机数不安全
    - buffer overflows
