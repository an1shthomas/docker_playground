```
$ docker pull coredns/coredns
$ docker run -d --name coredns --restart=always -v $(pwd):/root/ -p 10053:53/udp coredns/coredns -conf /root/Corefile

$ dig @127.0.0.1 -p 10053 server.example.com

$ nslookup -port=10053 server.example.com 127.0.0.1
```
