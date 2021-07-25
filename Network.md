# IPv4
## IPv4가 하는 일
네트워크 상에서 데이터를 교환하기 위한 프로토콜  
데이터가 정확하게 전달될 것을 보장하지 않는다. -> 멀리 있는 곳까지 전달만  
## IPv4의 구조

![ipv4](https://user-images.githubusercontent.com/51018201/126889764-22b2d1fd-93d8-4729-9f80-548a103d44ae.jpg)  

● Version : 4가 온다  
● IHL(Header Length) : 헤더의 길이는 20-60 따라서 4로 나눠서 20-60 -> 5-15로 표현  
● Type of Service(TOS) : 0으로 비워둠(요즘은 사용하지 않음, 예전은 중요한 데이터 유무 표현)  
● Total Length : 상위에서 캡슐화되어 내려온 길이와 합친 전체 길이를 의미  
● Identification : 원래의 데이터가 쪼개져서 전달될 때 ID가 같아야만 원래 동일한 정보였다는 판별함(동시에 여러개의 데이터를 전달받을 때)  
● IP Flag : D(1로 데이터를 안쪼개서 보내겠다를 지정->전송이 안됨), M(잘게잘게 쪼개서 보낼 때 내 뒤에 데이터가 더 있다를 알려줌 – 조각화될 때)  
● Fragment Offset : 받는 쪽에서는 순서가 꼬일 수 있으므로 원래대로 복구할 때 데이터의 순서를 지정(Offset – 맨 처음부터 얼마만큼 떨어져 있다)  
● Time To Live(TTL) : 패킷이 살아있을 수 있는 시간을 지정(패킷의 목적지가 잘못 설정되었을 때를 대비, 상대방의 운영체제를 추측 가능 -> 운영체제마다 TTL이 다름)  
● Protocol : 상위 프로토콜이 뭔지 알려줌(ICMP : 01 , UDP : 17 , TCP : 06)  
● Header Checksum : 헤더가 오류가 있는지 유무를 판별(내가 받은 헤더의 값을 이용해 계산하여 헤더 체크섬과 비교함)  

# ICMP
## ICMP가 하는 일
ICMP(Internet Control Message Protocol, 인터넷 제어 메시지 프로토콜)  
상대방과의 통신이 되나 안되나 확인하는 프로토콜  
## ICMP 프로토콜의 구조

![icmp](https://user-images.githubusercontent.com/51018201/126889967-5b3f8ffe-f0d5-49ac-929f-90e7e491f532.jpg)
![icmp_세부](https://user-images.githubusercontent.com/51018201/126889977-17ee6293-7030-43f4-bc72-d5cd88d76e78.jpg)

● Type : 카테고리(대분류), 0,8(0: 응답, 8: 요청), 3,11(3: 목적지 도달 불가 – 경로 설정 오류, 11: 요청 시간 만료 – 상대방의 문제일 가능성이 높다), 5(5: ICMP redirect – 상대방의 라우팅 테이블 원격 수정 가능 – 악용 가능성)  
● Code : Type의 소분류  
● Checksum : ICMP 헤더가 오류가 있는지 유무를 판별  


