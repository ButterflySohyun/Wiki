# WORDS

1. 클래스(Class) 
객체를 만들어 내기 위한 설계도 혹은 틀
연관되어 있는 변수와 메서드의 집합

2. 객체(Object)
소프트웨어 세계에 구현할 대상
클래스에 선언된 모양 그대로 생성된 실체
'클래스의 인스턴스(instance)'

3. 인스턴스(Instance)
설계도를 바탕으로 소프트웨어 세계에 구현된 구체적인 실체
객체를 소프트웨어에 실체화 한 것
메모리에 할당됨
인스턴스는 객체에 포함됨
복제본

ex) 객체는 클래스의 인스턴스다
	객체 간의 링크는 클래스 간의 연관 관계의 인스턴스다
	실행 프로세스는 프로그램의 인스턴스다
	즉, 인스턴스라는 용어는 반드신 클래스와 객체 사이의 관계로 한정지어서 사용할 필요는 없다.


추상화 기법
분류(Classification)
	객체 -> 클래스
	실재하는 객체들을 공통적인 속성을 공유하는 범부 또는 추상적인 개념으로 묶는 것
인스턴스화(Instantiation)
	클래스 -> 인스턴스
	분류의 반대 개념. 범주나 개념으로부터 실재하는 객체를 만드는 과정
	구체적으로 클래스 내의 객체에 대해 특정한 변형을 정의하고, 이름을 붙인 다음, 그것을 물리적인 어떤 장소에 위치시키는 등의 작업을 통		해 인스턴스를 만드는 것을 말한다.
	‘예시(Exemplification)’라고도 부른다.


4. JPA : Java Persistent(지속성 있는)  API

5. API(Application Programming Interface, 응용 프로그램 프로그래밍 인터페이스)는 
    응용 프로그램에서 사용할 수 있도록, 운영 체제나 프로그래밍 언어가 제공하는 기능을 제어할 수 있게 만든 인터페이스를 뜻한다. 주로 파일 제어, 창 제어, 화상 처리, 문자 제어 등을 위한 인터페이스를 제공한다.



----------------------------------------------------------------------------------------------------------------------------

용어

1. CORS  (cross-origin resource sharing)  :  http 접근제어// Cross-Origin Resource Sharing 표준은 웹 브라우저가 사용하는 정보를 읽을 수 있도록 허가된 출처 집합를 서버에게 알려주도록 허용하는 HTTP 헤더를 추가함으로써 동작합니다.

2. daemon: 멀티태스킹 운영 체제에서 데몬은 사용자가 직접적으로 제어하지 않고, 백그라운드에서 돌면서 여러 작업을 하는 프로그램을 말한다.

3. dev : development/ developer


4. JDBC(Java Database Connectivity)는 자바에서 데이터베이스에 접속할 수 있도록 하는 자바 API이다. JDBC는 데이터베이스에서 자료를 쿼리하거나 업데이트하는 방법을 제공한다.


5. DBCP는 DataBase Connection Pool 의 약자로 DB와 커넥션을 맺고 있는 객체를 관리하는 역할을 합니다.
JDBC만을 사용할 경우라면 DB접속 시 아래와 같은 순서가 반복되게 됩니다.

1. DB 접속을 위한 JDBC 드라이버 로드
2. getConnection Method로 부터 DB 커넥션 객체를 얻음
3. 쿼리 수행을 위한 PreparedStatement 객체 생성
4. excuteQuery를 실행해서 결과를 받아옴.
 
여기서 비효율적인 부분은 1번과 2번 입니다.
DB 연결 시 마다 Driver를 로드하고 커넥션 객체를 얻는 작업을 반복하죠.
이 부분을 효율적으로 처리하도록 바꾸는 것이 DBCP의 역할 입니다.

DBCP를 사용하게 되면,
WAS 실행 시 미리 일정량의 DB Connection 객체를 생성하고 Pool 이라는 공간에 저장해 둡니다.
그리고 DB 연결 요청이 있으면, 이 Pool 이라는 공간에서 Connection 객체를 가져다 쓰고 반환 하게 됩니다.

6. Impl : 실제구현체.

7. ORM : 객체 관계 매핑. 
     ORP와DB간 호환x, data를 변환하는 기법. 

8. entity 
    sql에서 실체, 객체

9. jpa transaction
    수동으로 jpa에 있는 함수(method) 말고 필요할 때.

10. junit 쓸때, @필요.
      browser로 확인 할때만 실제로 server실행.

11. 쿼리문 실제로 작성 x -> controller에 가까운 service에서 작성.

12. Singleton
인스턴스를 한 번만 만들기
인스턴스가 절대적으로 한개만 존재하는 것을 보증하고 싶을 경우. 두 번째 호출부터 인스턴스 로딩 시간이 줄어든다.
static 클래스와 다르게 초기화 Logic이 필요하고, 이를 계속 같은 초기화 Logic으로 사용할 때.

(1). Basic: 가장 기본적인 방법. 프로그램 시작하자마자 초기화
	만약 초기화 로직이 무거운 작업을 수행한다면 프로그램 실행시 대기 시간 길어짐.

(2). LazyInit: Client 쪽에서 호출될 떄 Singleton 자체의 초기화(=게으른 초기화)
	Thread-unsafe

(3). DCL: Double Checked Locking
	느리다

(4). Holder: Initialization on demand holder idiom
	클래스안에 싱글톤을 생성하는 static 클래스를 두어 JVM Class Loader 매커니즘과 Class가 로드되는 시점을 이용한 방법.
       Lazy Initialization 방식을 가져가면서 Thread간 동기화문제를 동시에 해결할 수 있다.
	Tread-safe
	ExceptionInInitializerError 발생 가능(특히 Android)

(5). Enum: "Effective Java"에서 소개된 방법.


13. <connection pool> 
 작업 순서

API 관련 jar 파일 설치 - lib폴더

DBCP 정보 설정 - context.xml

JNDI 리소스 사용 설정 - web.xml

자바 혹은 JSP 페이지에서 사용


----------------------------------------------------------------------------------------------------------------------------

jsp 용어 

jsp 파일을 실제 웹사이트에서 구동시키기 위해서는 웹사이트를 배포(실제서버에서 운영, 도메인 ㅇㅇ)해야 한다.

카페 24 웹 포스팅 

BBSDAO와 USERDAO 의
dbURL ID, PW 를 정한 값으로 바꾼다.

웹 포스팅 서비스 이용
jdk 다운그레이;드 




 DAO(데이터 접근 객체): 데이터 베이스에 접근해서 데이터를 빼올수 있는 기능을 한다.
jsp -----> database table

세션 : 회원 고유의 아이디 

자바 빈즈 : 하나의 게시글 정보를 담을 수 있는 인스턴스를 만들기 위한 틀이다. 
데이터베이스 테이블과 흡사한 구조를 가지고 있다. 
