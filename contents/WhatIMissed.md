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

e) HTTP의 구성 ( header, body..)
[e에 대한 Answer](#e에-대한-Answer)  


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
e) HTTP의 구성 ( header, body..)
#


*********
