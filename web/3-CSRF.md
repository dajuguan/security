# Cross-Site Request Forgery
被攻击者浏览器被迫向目标站点发起伪造请求，这个过程浏览器会带上呗攻击者的身份验证信息通过目标站点验证。

## 与XSS的区别
- XSS主要是利用网站自身的漏洞，来注入脚本，获取用户的敏感信息等
    - 但是一旦设置可HTTP only等字段，那么XSS就没法获取cookie了
    - XSS是自动的脚本会在目标站点自动运行，和其他站点无关
- CSRF则是需要交互才能发起请求，因此要么访问其他网站页面里面包含自动运行的脚本，要么在目标站点诱导用户点击响应按钮，或利用XSS注入组合攻击
    - 自动并不关键，因为恶意页面也可以设置表单自动提交的按钮
- 即使加入CSRF token防御，如果用XSS漏洞还是无法避免CSRF攻击，此时
    - 如果设置了httponly，则只能进行CSRF攻击
    - 如果没有，则可以进行XSS/CSRF攻击