

### Redis Gui Tool Download

https://www.electronjs.org/apps/p3x-redis-ui


### 외부 접속
```
내IP 확인방법 : Naver에서 "ip주소" 검색 

## VPC 등록

VPC -> 내가 사용한 VPC선택 -> 방화벽 탭
출발주소 : My Window IP
목적지주소 : redis 외부 IP  0.0.0.0/0
Port : TCP 6378


## Security Group 등록

Security Group -> 내가 사용한 SG 선택 -> 규칙 -> 규칙추가
inbound
대상주소 : My Windown IP
Port : TCP 6378 
```

### CRUD

* Create   
set key value

* Read   
get key

* Update   
set key value2
get key   

* Delete   
del key   

* Scan All Key   
key *


### TTL

set key value

ttl key

expire key 100

ttl key


