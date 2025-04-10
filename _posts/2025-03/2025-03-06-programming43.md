---
layout: post
title: "programming Day-43"
---

# programming Day-43

[2025-03-06-THU]

**JSP**
MVC 2 패턴
	redirect
- 요청경로 != 응답경로
- request(요청)객체를 모두 잃어버린다.
  쿼리스트링값을 사용할 수 없다.

- select후 답이 있다면 쿼리스트링에 담기


forword
- 요청 == 응답
- request객체를 잃어버리지 않는다.
   ex) 상세 정보 조회 
- 어떤 값들을 다른 suvlet으로 보낼때 사용

- request에 담기


FrontController
사용자의 요청에 확장자가 붙는데, 
그 확장자에대한 분류를 처리한 후 맞는 컨트롤러로 보내주는 역할



