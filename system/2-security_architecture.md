## security architecture: defend classes of attacks even unknown attack
- google:
    - end-user data
    - availability
    - accountability
- threats:
    - bugs
    - passwd theft
    - insider
    - hardwork
    - network
    ...

谷歌那样的大型架构是如何实现的:
- Isolation
    - 手段:VMS/物理隔离
- Sharing: reference model/guard model
    - principle(enduser/employee/service/machine) -> request-> guard(注入policy，并单独存放audit log) -> resource (data, bandwith, CPU)
    - guard:
        1.authentication: password/2FA/IP/公私钥
        2.authorization: check policy = Policy(principle, resource)
            granuality: 
                - DC(data center): firewall/IDS入侵检测
                - service: least privilege
        3.audit

### hardware

### Avaliability: DDOS


