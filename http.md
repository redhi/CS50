# http
## HTTP 요청 프로토콜
- 요청하는 방식을 정의하고 클라이언트의 정보를 담는다  
- 영어와 특수문자로 작성  
## HTTP 요청 프로토콜의 구조
![http_request_protocol](https://user-images.githubusercontent.com/51018201/128588852-f9227b86-5a44-4de0-bb5f-dc59a920e849.jpg)
![http_request_protocol_ex](https://user-images.githubusercontent.com/51018201/128588851-e344fb9d-6a54-4529-9c57-63cb4206c374.jpg)

- Request Line : 빨간색 상자  
![http_request_line](https://user-images.githubusercontent.com/51018201/128588853-f3487491-5bb5-4908-a97c-c7c464cf221c.jpg)
![http_request_form](https://user-images.githubusercontent.com/51018201/128588850-57149ccb-2dbe-4e7c-b184-e7a2cd31d9c2.jpg)
  - 요청 타입 : GET(Client가 Server한테 어떤 데이터를 보내달라고 요청하면서 데이터를 보낼 수 있다), POST(Client가 Server에게 어떤 정보를 전송할 때 사용하면서 요청할 수 있다)  
    -> COPY, MOVE, DELETE는 사용자가 임의로 서버의 데이터에 손상을 주지 못하게 서버 측에서 막아 놓는다  
    -> GET과 POST를 왜 나눠놨는가?  
      - GET 방식은 데이터를 보낼 때 uri부분에 데이터를 포함시켜 보낸다(노출되어도 되는 데이터)
      - POST 방식은 데이터를 보낼 때 body부분에 데이터를 포함시켜 보낸다(중요한 데이터)
    ![http_uri_structure](https://user-images.githubusercontent.com/51018201/128588849-b1e4f31c-b854-4a4f-addd-2c1f60228745.jpg)

  - URI(Uniform Resource Identifier) : 인터넷상에서 특정 자원(파일)을 나타내는 유일한 주소
	- URI의 구조   
		  - 스키마 : http, https, ftp 등 프로토콜  
		  - 포트번호 : 지정하지 않고 웹 브라우저가 알아서 지정(80, 443)  
		  - 경로 : 원격지의 폴더 내에 파일을 지정  
		  - 쿼리 : 원하는 데이터를 전달하는 값  

- Headers : 파란색 상자, 다양한 옵션을 나타냄
- 공백 : 초록색 상자, 한 줄의 공백을 표시
- Body : 주황색 상자, 어떤 데이터를 요청할 때 들어가는 값
