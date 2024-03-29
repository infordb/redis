

### Redis Gui Tool Download

https://www.electronjs.org/apps/p3x-redis-ui


## 외부 접속
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

## Redis info

```
> info
```


## CRUD

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
keys *


### TTL (Time To Live)

set key value

* ttl 적용 확인   
ttl key

* ttl 적용   
expire key 100

ttl key

SET anotherkey "will expire in a minute" EX 60   


## Sorted SET
Sorted Sets는 key 하나에 여러개의 score와 value로 구성됩니다.   
Value는 score로 sort되며 중복되지 않습니다.   
score가 같으면 value로 sort됩니다.   
Sorted Sets에서는 집합이라는 의미에서 value를 member라 부릅니다.   
Sorted Sets은 주로 sort가 필요한 곳에 사용됩니다.   

* sorted set 생성   
zadd mysite  1000 google.com 900 facebook.com 800 youtube.com   

* Score 역순 조회    
zrevrange mysite 0 -1 withscores   

* youtube.com score 150 증가   
zincrby mysite 150 youtube.com       

* Score 역순 조회    
zrevrange mysite 0 -1 withscores   

* google.com score 60 감소   
zincrby mysite -60 google.com   

* Score 역순 조회    
zrevrange mysite 0 -1 withscores   

* 조회개수
```
* 0 -1 전체 조회
zrange mysite 0 -1 withscores
* 0 0  1개 조회
zrange mysite 0 0 withscores   
* 0 1  2개 조회
zrange mysite 0 1 withscores
```
* ASC 조회   
zrange mysite 0 -1 withscores
