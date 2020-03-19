# JAVA
<br> final 상수, static 하나의 클래스에서 공유o
<br> (cast) 형변환 
<br> substring 자르기
<br> main method에서 함수 쓰려면 함수에도 static 붙여야 해.
<br> string 비교할때 equal() 사용. why? 문자열 자료형이기 때문! 클래스기반.
<br> java에서 class는 곧 자료형이다.
<br> input, output -> File file / 기본 입출력, file 입출력.
<br> java에서 함수 = method.
<br> 재귀함수 -> 매력적이지만 너무 많은 연산, 비효율 -> 해결 -> 동적프로그래밍.
<br> 배열 <- data가 많을때.
<br> 
<br> class: 사물의 특징을 살려서 '틀'만듬. -> 인스턴스화 -> 객체
<br> 상속 ->> 객체지향
<br> super() : 부모클래스의 생성자를 실행하겠다.
<br> 클래스, 상속 / 생성자로 초기화.
<br> OOP의 설계기법
<br> 추상화 : 설계적부분 / 인터페이스
<br> 추상클래스(미완클래스, 밑바탕, 설계틀) - 객체 인스턴스 생성x
<br> 추상클래스(체계적 설계) --> 상속받은 추상 메소드는 반드시 구현해야함.
<br> main static 안에서 불러오는 메소드들도 static으로 선언되어 있어야한다.
<br> @Override : 재정의
<br> 추상클래스 : 내가 어떤 메소드(함수)를 써야하는지 명시해줌.
<br> 
<br> Final 키워드 : 절대변하지 않음. 변수(변하지 않음, 상수), 메소드(재정의 불가,) 클래스(상속 불가) 모두 사용가능.
<br> Interface : 더 빡빡하게 설계하고 압박. 다중상속 구현가능. 추상클래스(어떤 메소드를 써야하는지 암시, 추상메소드 외에 멤버변수와 일반메소드 가질수 있음)보다 더 추상적이다.
<br> 인터페이스는 implements로 상속. only설계만 , 추상메소드와 상수만가질수 있다. 일반메소드x, 실질적 코드x. 더 엄격한 추상화!
<br> Main main = new Main() 메인메소드에 인스턴스만듬O
<br> 
<br> 다형성 : 다양한 형태의 성질을 가진다.
<br> 객체를 사용할때 사용하는 변수 형태를 바꾸어 여러타임의 객체를 참조할 수 있다. 
<br> 소스를 유연하게 구성가능. 
<br> 부모클래스 타입의 참조변수로 하위 클래스의 객체를 참조할 수 있게o.
<br> Fruit fruit(부모변수, 자기자신 변수내용 바꿀수 있다) = new Peach() 자식, 부모를 상속, 자식클래스의 인스턴스 변수를 부모의 변수로 넣을 수 있다. 
<br> 객체(실세계 사물이라는 객체) object 클래스, 모든 객체의 조상
<br> 모든 클래스는 object 클래스를 상속o(내부적으로) 모든 클래스가 공통으로 가지고 있어야하는 기능을 포함하고 있다.
<br> (자식) 부모 . (Archer) ojt 
<br> Tip, 내부변수가 같더라도 equals로 비교. 두 인스턴스가 다르기 때문.
<br> Super (부모 내부 변수) : 부모 클래스의 생성자.
<br> instance of~  ~의 인스턴스?
<br> Warrior temp 자식= (형변환 Warrior) heors 부모
<br> 다형성 : 그때 그때 필요한 변수를 할당. 
<br> 
<br> jsp 서버 프로그램언어 / java언어 사용.
<br> jsp 웹서버 <ㅡ tomcat
<br> startup.bat
<br> 웹사이트 개발환경 - eclipse 서버관리o, JavaEE
<br> 
<br> jsp Dynamic Web project
<br> meta 반응형 웹
<br> 디자인 -> bootstrap
<br> 에니메이션 <- jquary.
<br> db -> jsp : java resource 폴더에 package class.
<br> java bean : 데이터를 표현하는 것이 목적.
<br> DA0 (데이터베이스 접근 객체)
<br> DTO
<br> conn, pstmt, rs 
<br> mysql - jdbc driver
<br> 
<br> 로그인기능구현 : session / 보안.
<br> post : 보내지는 내용 숨겨진다.
<br> 
<br> 배포 : web posting service!
<br> cafe24, 파일질라o, r드라이브, Putty -> 자기 웹서버에 접속. ssh
