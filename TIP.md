# TIP

0. 모르면 자꾸 물어볼 것 
    작은것이 문제
    작은 issue, 수행사항 --> gitlab에 기록하기 / trello에 기록or계획 하기 

1. source --> 변경된 소스 적용
    ex) source /etc/profile
            source ~/.profile
2. 회사 서버
192.168.0.48
미래기후/ alforlgn!
중기청 아이디 :  MIRAESOHYUN

3. 내 local port 
192.168.1.77

4. db생성할 때 개발 포트 열기 

5. 동등성 비교
HashCode / equals.
--> 동등성 만들고 싶을 땐 둘 다 구현해야 한다. 

6. 404error -> server 쪽 에러
   url path check 해보기 

7. eclipse -> workspace 기반 
    intellij -> project 기반, 같은 dir이면 안된다.

8. is~(f) {  
  
} return --->(true/false)

9. Field userRepository in com.example.memo2.service.UserService required a bean of type 'com.example.memo2.repository.UserRepository' 
that could not be found. The injection point has the following annotations: - @org.springframework.beans.factory.annotation.Autowired(required=true)

==> main함수에  @EnableAutoConfiguration(exclude={DataSourceAutoConfiguration.class})      제거 

 @EnableAutoConfiguration이라는 어노테이션은 스프링부트에서 미리정의해둔 bean 설정(configuration)들을 사용하게되어서 우리는 아무설정없이 SpringBoot를 이용하는 것 처럼 보이게 되는 것이다.

10. REST test

Default HEADER 
Content-Type : application/json

ng serve --proxy-config proxy.conf.json


11.처음 spring project pom.xml  에 error날 때

<>  추가!


12. h2

spring.h2.console.enabled=true
spring.h2.console.path=/test_db

spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.url=jdbc:h2:file:./test.db 
spring.datasource.username=test
spring.datasource.password=1234

spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
