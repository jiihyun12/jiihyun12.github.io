---
layout: post
title: "programming Day-68"
---

# programming Day-68

[2025-04-10-THU]


Spring MVC(Front-Controller 패턴)

         HandlerMaping
REQUEST        ①         ②↕      ③             ④
   ]     ↔   DispatcherServlet   ↔  HandlerAdapter   ↔  Controller
RESPONSE     ⑦   ⑥↕        ⑤↕
         View   ViewResolver
            ↕
         HTML 및 기타

-------------------------------------------------------------------------------------------------
Spring MVC 패턴의 특징
   - HttpServletRequest, HttpServletResponse를 거의 사용할 필요 없이 기능 구현
   - 다양한 타입의 파라미터 처리, 다양한 타입의 리턴 타입 사용 가능
   - GET 방식, POST 방식 등 전송 방식에 대한 처리를 어노테이션으로 처리 가능
   - 상속/인터페이스 방식 대신 어노테이션으로만 설정 가능
-------------------------------------------------------------------------------------------------



================================================================
[개인 메모]
스프링에서 사용되는 편리한 MVC 패턴
FC와 XMl이 필요없다


요청이 들어온다.  - dispatcher Servle이 찾는다. - handlerMapping이 도와준다. -> 스캔, controller 
handlerAdapter를 통해 방금 보고받은 controller를 실행시킨다.
resolve

컨트롤러의 리턴값은 문자열 또는 void 
컨트롤러를 응답해줄 수 없기때문에 문자열 또는 경로로 받는다.

내가 할 것은 컨트롤러를 만들고 보고하는 것밖에 없다.

=====
컨트롤러를 만들고 컨트롤러인것을 알려주는 어노테이션을 붙인다ㅣ(보고)
mybatisApplication에서 서버를 실행시킨다.
브라우저로 가서 localhost10000 -->우리의 포트 번호, 뒤의 URI는 우리가 설정했던 test/ex 로 들어가서 실행 결과를 확인한다.



Model 객체
	- Controller에서 생성된 데이터를 담아서 View로 전달할 때 사용되는 객체
	- Servlet의 requser.setAttribute()와 유사한 역할
	-adAttribute(key, value) 메소드를 사용하여 전달할 데이터를 세팅



----------------------------------------------------------------------

타임리프(thymeleaf)의 사용 문법
   - th:text="${}" : 단순 텍스트
   - th:src="${}" : 이미지 src
   - th:href="@{}", th:href="||" : 하이퍼텍스트 링크
      <a th:hrf="@{/mypage?userNum={num}}"></a> // 파라미터 넘길경우
        <a href="@{/user/profile(param=${param})}"></a> // 파라미터 넘길경우
        <a href="@{user/product/{param1}(param2=A, param3=B)}"></a> 

   - th:value="${}" : input value
   - th:if="${}", th:unless="${}" : if~esle이나 조건이 같아야한다.
      <a href="/product" th:if="${session.userAuth == '1'}">상품등록</a>
      <a href="/product" th:unless="${session.userAuth == '2'}">상품등록</a>
   
   
   - th:each="변수 : ${list}" : 빠른 for문
      <div th:each="user : ${userList}">
         <span th:text="{user.username}">username</span>
             <span th:text="user.age}">age</span>
      </div>
   
   - th:switch, th:case : 스위치문
      <th:block th:switch="${userNum}"> 
          <span th:case="1">권한1</span> 
           <span th:case="2">권한2</span> 
      </th:block>



-----

세션 영역에 flush라는 영역이 있다.
세션은 서버 저장소이기때문에 로그아웃이 되기 전까지는 저장된 데이터는 사라지지 않는다
세션은 서버쪽에 많은 부담을 주고있다
flush영역은 request처럼 


-----


작업 순서

1. DB 테이블 & 시퀀스 생성
2. domain 패키지 안에 VO 클래스 생성
3. Mapper에 SQL 작성 (namespace에 경로 설정)
4. config.xml(MyBatis 설정 파일)에 타입 알리아스 설정
5. 인터페이스 생성
6. Controller 클래스에서 GET / POST 매핑
7. templates  폴더에서 html 화면 작성
8. Test 실행 → log로 확인
9. 브라우저에서 요청 → 화면으로 확인


공통 사항

클래스를 만들었다면 스프링에게 "이 클래스 써라"라고 보고해야한다.

클래스를 스프링에 등록

어노테이션		역할				보고(누구에게)

@Controller		컨트롤러로 등록			스프링 MVC
@Component		클래스 등록			스프링 컨테이너
@Mapper			MyBatis Mapper로 등록		MyBatis + 스프링

@Autowired		스프링한테 Bean 주입해달라고 요청	스프링
@Test			테스트 메서드임을 알려줌		JUnit

@RequestMapping,	요청 URL과 메서드 연결		스프링 MVC 디스패처 서블릿
@GetMapping,
@PostMapping






