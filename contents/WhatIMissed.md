# What I Missed

### **:radio_button: Questions** 
a) Join이 무엇인가? Join의 종류에는 어떠한 것들이 있는가?  
[a에 대한 Answer](#a에-대한-Answer)  

b) 데이터 베이스에서의 PK, FK에대해 자세히 말해보아라  
[b에 대한 Answer](#b에-대한-Answer)  

c) 4handway shaking 에대해 자세히 말해보아라 ( close, wait등을 포함하여)  
[c에 대한 Answer](#c에-대한-Answer)  

d) 자바의 Static에 대해 설명하라  
[d에 대한 Answer](#d에-대한-Answer)  

e) HTTP  
[e에 대한 Answer](#e에-대한-Answer)  

f) 인터페이스와 추상 클래스  
[f에 대한 Answer](#f에-대한-Answer) 

g) DBMS(Oracle) 의 Hint
[g에 대한 Answer](#g에-대한-Answer) 

h) JAVA 묵시적 형변환과 명시적 형변환
[h에 대한 Answer](#h에-대한-Answer) 


*********
## a에 대한 Answer
* a) Join이 무엇인가? Join의 종류에는 어떠한 것들이 있는가?
#
* join의 개념
    * join이란 두 개 이상의 테이블이나 데이터베이스를 연결하여 데이터를 검색하는 방법이다. RDBMS는 최소한의 데이터를 테이블에 담고 있으며, 원하는 정보를 검색하기 위해서는 테이블 간의 연결고리로 관계를 맺고 데이터를 추출해야하는데, 이때 Join이 사용된다.  
    * 보통 PK 및 FK값을 사용하여 join한다. 
    * join은 join 연산자에 따라, From 절의 join 형태에 따라 구별할 수 있다.  

* join의 종류
    * Inner Join  
    1. EQUI Join ( 동등 조인 )
        * join 대상 테이블의 칼럼값들이 서로 정확하게 일치하는 경우 join으로 WHERE 절에 '='(equality. condition)을 사용하여 JOIN 조건을 명시한다.  
    
    2. Natural Join
        * EQUI Join에서 Join 조건이 '='일 때 동일한 속성이 두번 나타날 때, 중복되는 것을 제거하여 같은 속성을 한번만 표기하는 방식.
        * Natrual Join의 단점은 동일한 이름을 가지는 칼럼은 모두 Join이 되지만, USING 문을 사용하면 칼럼을 선택해서 join 할 수 있다. Using 절 안에 포함되는 칼럼에 Alias를 지정하면 오류가 발생한다.  
    
    3. Non EQUI Join
        * Join 대상 테이블의 어떤 칼럼값도 일치하지 않을 때 사용하고, '=' 이외의 연산자를 상요한다.    
    
    4. Self Join
        * 같은 테이블에서 2개의 속성을 연결하여 Equi Join을 하는 것이다.  
    
    * Outer Join
        * Join 조건을 만족하지 않는 데이터를 처리하기 위한 Join으로, Inner join이 두 테이블에 있는 일치하는 값만 가져오는 것에 비해, outer join은 어느 한쪽의 데이터를 모두 가져온다.
        * Join 조건에 일치하지 않는 값을 추가할 때 사용한다.  
    
    1. Left Outer Join
        * Join 수행 시 왼쪽에 표기된 데이터를 기준으로 Outer Join을 수행한다.  
    2. Right Outer Join
        * Join 수행 시 오른쪽에 표기된 데이터를 기준으로 Outer Join을 수행한다.  
    3. Full Outer Join
        * Join 수행 시 왼쪽, 오른쪽 테이블의 모든 값을 읽어 JOIN을 수행한다.  LEFT Outer join과 Right Outer Join의 결과를 합집합으로 처리한 결과와 동일하다.  
    
>  http://all-record.tistory.com/160
>  http://server-engineer.tistory.com/306

            

*********
## b에 대한 Answer
* b) 데이터 베이스에서의 PK, FK에대해 자세히 말해보아라 
#
1. Primary key(PK)
    * 한 row를 대표하는 키이며, 중복된 값을 허용하지 않는다. 
    * primary key가 여러개일 수도 있으며, 이럴 때는 두개가 똑같이 중복될 경우에만 중복값으로 생각한다.
    
2. Foreign Key(FK)
    * Foreign key는 다른 테이블의 PK를 컬럼으로 가지고 있는 것으로, 중복이 가능하다.
    * 한 테이블의 키 중 다른 테이블의 행(row)를 식별할 수 있는 키이다. 
    * PK와 FK는 1:다 관계이다. 

>  http://ande226.tistory.com/56
>  http://woodforest.tistory.com/120

*********
## c에 대한 Answer
c)  4handway shaking 에대해 자세히 말해보아라 ( close, wait등을 포함하여 )
#

 *********
## d에 대한 Answer
d) 자바의 Static에 대해 설명하라
#
1. Static 변수
    * 클래스 변수로, 클래스가 정의만 되어도 접근이 가능한 변수이다. 
    * 변수에 Static 키워드를 붙이면, 메모리 할당을 딱 한번만 하게 되어 메모리 사용에 이점을 볼 수 있게된다. 
    * static 으로 설정하면 같은 곳의 메모리 주소만을 보기 때문에 static 변수의 값을 공유하게 된다. 
    * 인스턴스 간에 데이터 공유가 필요한 상황에서 쓰임 ( singleton 패턴과 비슷함)
    
2. Static 메서드
    * 클래스가 정의만 되어도 사용할 수 있는 메서드이다.
    * Class.staticmethod() 형식과 같이 클래스를 통해 호출할 수 있다.
    * Static 메소드 안에서는 인스턴스 변수 접근이 불가능하다. 

Static은 반드시 메모리에 올라가며, Garbage Collector의 대상이 되지 않는다. 객체를 다시 생성한다고 해도, 그 값은 초기화 되지 않고 해당 클래스를 사용하는 모든 객체에서 공유하게 된다.  


>  https://wikidocs.net/228
>  https://m.blog.naver.com/PostView.nhn?blogId=ndb796&logNo=221203398703&proxyReferer=https%3A%2F%2Fwww.google.co.kr%2F
*********
## e에 대한 Answer
e) HTTP
#

**1. HTTP에 대하여**  
HTTP(Hypertext Transfer Protocol)는 인터넷 상 데이터를 주고받기 위한 서버/클라이언트 모델을 따르는 
프로토콜이다. 어플리케이션 레벨의 프로토콜로 TCP/IP 위에서 작동한다.  
Hypertext가 붙은 이유는 하이퍼텍스트 기반으로 데이터를 전송하겠다는 뜻으로, 링크기반으로 데이터에 접속하겠다는 의미이다.  
  
**2. Connectless & Stateless**  
HTTP는 **Connectless** 방식으로 작동된다. 즉, 서버에 연결하고, 요청해서 응답을 받으면 연결을 끊어버린다. 기본적으로 자원 하나에 대해 하나의 연결을 만드는데 이러한 작동 방식은 각각 이러한 장단점을 가진다.  

* 장점 
    * 불특정 다수를 대상으로 하는 서비스에 적합하며, 많은 수의 클라이언트가 웹 서비스를 이용하더라도 접속 유지는 최소한으로 할 수 있기 때문에, 더 많은 유저의 요청을 처리할 수 있다.  
* 단점 
    * 연결을 끊어버리기 때문에, 클라이언트의 이전상태를 알 수가 없다. 이러한 HTTP 특징을 **Stateless**라고 하는데, 이는 Connectless로 부터 파생되는 특징이다.
    * 클라이언트의 이전 상태 정보를 알 수 없게 되면, 웹서비스를 하는데 문제가 생기는데, HTTP는 **cookie**를 이용하여 이러한 문제를 해결한다.  
    
**3. URI**  
클라이언트 프로그램(웹 브라우저)는 URI를 이용하여 자원의 위치를 찾는다. URI는 HTTP와는 독립된 다른 체계이다. HTTP는 전송 프로토콜이고, URI는 자원의 위치를 알려주기 위한 프로토콜이다.  	
URI는 "Uniform Resource Identifiers"의 줄임말로, World Wide Web 상에서 접근하고자 하는 자원의 위치를 
나타내기 위해서 사용한다. 이때, 자원은 문서, 이미지, 동영상, 프로그램, 이메일 등이 될 수 있다. 메일을 받을 상대방의 위치를 나타내기 위하여 사용되는 email://tedigom7@gmail.com , 웹페이지의 위치를 나타내는 https://www.github.com/tedigom 등이 URI의 예이다.  

**4. Method**  
* GET : 정보를 요청하기 위하여 사용한다.(SELECT)
* POST :  정보를 밀어넣기 위하여 사용한다. (INSERT)
* PUT : 정보를 업데이트하기 위하여 사용한다. (UPDATE)
* DELETE : 정보를 삭제하기 위하여 사용한다. (DELETE)
* HEAD : (HTTP의) 헤더 정보만 요청한다. 해당 자원이 존재하는지, 혹은 서버에 문제가 없는지 확인하기 위해서이다.
* OPTIONS : 웹서버가 지원하는 메서드의 종류를 요청한다.
* TRACE :  클라이언트의 요청을 그대로 반환한다. 예를들면 echo 서비스로 서버상태를 확인하기 위한 목적으로 주로 사용한다.

하지만 보통의 웹서비스는 GET과 POST만을 이용하여 개발한다. GET과 POST 만으로 모든 종류의 요청을 표현할 수 있기 때문이다.  

**5. 요청 데이터 포맷 (Request Data format)**  
웹 브라우저는 웹 서버에 데이터를 "요청(request)" 하는 "클라이언트 프로그램"이다. 요청은 서버가 인식할 수 있는 형식(HTTP 형식)을 따르는데, 요청 데이터는 "HEADER"와 "BODY"로 구성된다

* **Header**
    * HTTP 헤더는 라인피드와 캐리지리턴(/r/n)을 함께 사용한다. HTTP 헤더를 파싱할 때 주의해야한다.  
    * 필수요소로 요청의 제일 처음에 와야한다. --> 3개의 필드로 이루어 져있다.(요청 라인)
        * 요청 메서드 : GET, PUT, POST, PUSH, OPTIONS 등의 요청 방식이 온다.
        * 요청 URI : 요청하는 자원의 위치를 명시한다.
        * HTTP 프로토콜 버전 : 웹 브라우저가 사용하는 프로토콜 버전.
        * ex ) GET / HTTP / 1.1     (GET 방식에서는 일반적으로 BODY가 없다.)
    * 맨 위에 요청라인 ( Request-Line)이 있고, 요청라인 다음줄에는 HTTP 헤더 정보가 포함된다. 
    * 헤더에는 요청라인 이외에도 Accept, User-agent, Host, If-Modified-Since, Refer, Cookie, Accept-Language, Accept-Encoding 등이 포함된다.
    * 헤더와 메세지 바디 사이에는 공백이 한줄 있는데, 이 한줄로 헤더와 바디를 구분한다.  
    
* **Body**
Body는 conetent type에 따라 나눌 수 있다.
    * form 형태 : URLEncoded 방식
        * application/x-www-form-urlencoded
        * 메세지 바디 : 쿼리 문자열
    * json 형태
        * application/json
    * 멀티파트 형태 : 이진파일 넘길때 사용되며, 하나의 메세지 바디에 파트를 나누어서 작성한다.
        * boundary는 파트 구분자
        * multipart/form-data:boundary=frontier
    
    
**5. 응답 데이터 포맷 (Response Data format)**  
* **Header**
    * 응답 데이터 포맷에는 프로토콜과 응답코드가 제일 처음 와야한다.
        * ex ) HTTP / 1.1 200 OK \r\n
        * HTTP/1.1 : 응답 프로토콜과 버전
        * 200 : 응답코드
        * OK : 응답메세지 - Not Found, Internal Server Error 등의 메세지이다.
    * 날짜, 서버프로그램 및 스크립트 정보, 컨텐츠 수정일,캐시 제어 방식, 컨텐츠 길이 등을 헤더에 포함한다.
    * Keep alive - 클라이언트 측에 연결을 유지하라는 신호로 보내기 위해서 사용한다. 그러면 클라이언트는 최대 timeout에 지정된 시간동안 연결을 유지한다. 이 시간동안 클라이언트는 이미 맺어진 연결로 요청을 계속 보낼 수 있다.  

**6. Keep Alive**  
HTTP 1.1 부터는 keep-alive 기능을 지원한다.  
  
HTTP는 하나의 연결에 하나의 요청을 하는 것을 기준으로 설계가 됐다. 요즘 웹 서비스의 경우 간단한 페이지라고 해도 수십개의 데이터 - 이미지, 문서, css, javascript 등이 있는데, HTTP의 원래 규격대로라면, 웹페이지 하나를 표시하기 위해서 연결을 맺고 끊는 과정을 수십번 반복해야한다. 이는 매우 비효율적이다.   
  
Keep-alive 설정을 하면, 지정된 시간 동안 연결을 끊지 않고 요청을 계속해서 보낼 수 있다.  
  
**7. 세션의 관리**  
HTTP를 기반으로 하는 웹 서비스는 connectless 방식으로 이전의 상태정보를 유지할 수 없는데, 결국 클라이언트의 상태 정보를 정보 조각 형태로 서버와 클라이언트에 남기는 방식으로 문제를 해결한다. 이 조각을 cookie라고 하고, 서버는 cookie를 이용하여 세션정보를 관리한다.  

> https://www.joinc.co.kr/w/Site/Network_Programing/AdvancedComm/HTTP
> http://withbundo.blogspot.com/search/label/HTTP?updated-max=2017-07-19T15:16:00%2B09:00&max-results=20&start=21&by-date=false
> https://blog.outsider.ne.kr/312

*********

## f에 대한 Answer
f) 인터페이스와 추상 클래스 사이의 차이점을 설명하라

* 인터페이스(interface)에서는 클래스와 별도로 일련의 연관된 메소드를 선언한다.
* 추상 클래스(abstract class)는 메소드를 선언하기는 하지만, 모든 메소드를 정의하지는 않는 불완전하게 정의된 클래스이다.
  
* 인터페이스와 추상클래스는 존재 목적이 다르다. 추상클래스는 그 추상 클래스를 상속받아서 기능을 이용하고, 확장시키는데에 있다. 반면 인터페이스는 함수의 껍데기만 있는데, 그 이유는 그 함수의 구현을 강제하기 위해서이다. 구현을 강제함으로 구현 객체의 같은 동작을 보장할 수 있다.

> https://loustler.io/languages/oop_interface_and_abstract_class/

*********

## g에 대한 Answer
g) DBMS(Oracle) 의 Hint에 대해 설명

* 힌트(hint)란?
    * 옵티마이저는 SQL문에서 최적의 실행계획을 제공한다. 하지만 잘못된 SQL 문이나 부정확한 통계정보로 인해 엉뚱한 실행계획을 제공할 때도 간혹 있는데, 이때 힌트절을 통해 잘못된 실행 계획을 바로 잡을 수 있다. 즉, Hint는 옵티마이저의 실수를 만회할수 있는 개발자의 마지막 무기라 할수 있다.
    * 즉, HINT는 실행하려는 SQL 문에 사전에 정보를 주어 SQL문 실행에 빠른 결과를 가져오라는 것이다. SQL 문 HINT를 사용하면 OPTIMIZER는 우선 SQL문의 HINT를 이용하고, 그다음 OPTIMIZER_MODE에 설정된 값을 이용한다.
    
    * SELECT /*+[힌트절]*/~  
    형태로 주석문 안에 힌트절을 표시한다. 따라서 잘못된 힌트절로 인해 에러를 리턴할 일은 없다. 다만, 힌트절의 내용대로 적용되지 않을 가능성은 있다. 
    
* 힌트의 종류
    * 접근 순서를 결정하는 힌트절
        * ORDERED : From 절에 나열된 테이블 순서대로 접근한다.(SQL문에 종속적)
        * LEADING : 테이블 접근 순서를 명시적으로 표시한다.(SQL문에 독립적)
    * 접근 방법을 결정하는 힌트절
        * USE_NL : Nested Loop join 방식으로 조인하도록 유도한다. (순차적인 접근 방법)
        * USE_HASH : Hash Join 방식으로 조인하도록 유도한다. ( 해시함수를 이용한 접근방법)
    * 자원 사용을 결정하는 힌트절
        * INDEX :  인덱스를 통한 Access path를 유도한다.
        * FULL : 테이블을 Full scan 한다.
        * PARALLEL : 병렬처리를 통해 성능을 높인다.


*********

## h에 대한 Answer
h) JAVA 묵시적 형변환과 명시적 형변환의 차이

* 묵시적 형변환 : 작은 데이터타입을 큰 데이터타입으로 변환하는 것.
    * ex) int a = 10;   double b = a;   --> 10

* 명시적 형변환 : 큰 데이터 타입을 작은 데이터타입으로 변환하는 것. 데이터 손실이 있을 수 있으며, 코드에 명시해 주어야 함.
* ex ) double a = 10.4D;    int b = (int)a;   --> 10


* 즉, 묵시적 == 자료의 확대형(광역화) == 컴파일러가 묵시적으로 시행,  
  명시적 = 자료의 축소형(협소화) == 프로그래머가 자료의 손실로 인한 명시적으로 시행
