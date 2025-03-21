---
layout: post
title: "programming Day-02"
---

# programming Day-02

[2024-12-31]

**HTML**
속성이란?
	- 하나의 태그를 여러 번 사용할 수 있으나, 
	다른 부분에서 그 태그를 구분할 때 구분점이 없어서 
	Key와 value(map구조)사용자들이 정보들을 넣으면 좋겠다고 생각해 만든 것이 속성이다.
	key=value 한 쌍으로 이루어져 잇어며, key는 정해져있고 value에따라 바뀐다.
 
 <hr/>
HTML 요소(element)의 종류
블록 요소
	- P, h1~6, ul, ol, div, form, table, ... 등
	- 코드 상에 한 주로 이어 써도 화면 상에서는 
	앞 뒤 요소 사이에 새로운 줄을 만들어서 나타낸다. 
	즉, 한 줄을 모두 사용한다.
	- width, height 속성을 자유롭게 수정할 수 있다.
	- margin, padding 속성도 잘 적용된다.
	- div 태그
		1. 다른 HTML 요소들을 하나로 묶는 데 사용되는 대표적인 블록 요소이다.
		2. 주로 여러 요소들의 스타일을 한 번에 적용하기 위해 div 태그를 사용한다.

인라인 요소
	- apsn, a, img, strong, em, ...등
	- 새로운 줄은 만들지 않고 작성한 다낙 내에 나타난다.
	- 안에 있는 내용 마늠의 영역을 차지한다.
	- width, height 속성을 자유롭게 수정할 수 없다.

인라인 블록 요소
	- button, input, select
	- inline 요소와 동일하게 내용만큼의 영역을 차지하지만 
	width, height를 자유롭게 수정할 수 있다.
	- padding, margin도 자유롭게 수정할 수 있다.

 <hr/>
시멘틱 태그
	- 의미가 있는 태그들로, html 문서 내의 가독성 개선과 외부 검색 엔진(SEO)에도
	내 문서 내의 어떤 부분이 메인인지 보여줄 수 있도록 최적화 시켜줄 뿐만 아니라, 
	개발자의 유지보수 및 웹 페이지를 시각적이 아니라 음성으로 읽어주는 "스크린리더"를
	이용할 때 웹 접근성을 유용하게 만들어주는 태그이다.

시멘틱 태그의 종류
	- header : 상단, 헤더를 의미
	- nav : 메뉴, 내비게이션을 의미
	- section : 여러 중심의 내용을 감싸는 공간을 의미
	- main : 내용의 중심을 의미
	- article : 글자가 많이 들어간 부분을 의미
	- aside : 사이드에 위치하는 공간을 의미
	- footer : 하단, 푸터를 의미

 <hr/>

*form 태그
	- 폼은 사용자가 웹사이트에 데이터를 전송해주기도 하며 
	이 밖에 웹 페이지가 입력 데이터를 사용하기 위하여 사용할 수도 있다.

1) 속성(Attiribute)란?
	- 태그에 추가로 정보를 제공하거나 
	태그의 동작이나 표현을 제어할 수 있도록 지정해주는 설정 값을 의미한다.

2) 속성의 사용 방법
	- 속성명= "속성값"

3) *표기법
	- 카멜 표기법(camelCase) : 낙타의 등을 본따 만든 표기법	
		주로 JAVA, JavaScript, C, ...언어에서 주로 사용된다

	- 파스칼 표기법(PaseCalCaxe) : 낙타의 등, 양봉을 본따 만든 표기법
		주로 JSVS, Pytho에서 사용된다.

	- 케밥 표기법(cabab-case) : 케밥을 본따 만든 표기법
		주로 HTML, CSS, ...언어에서 사용된다.

	- 스네이크 표기법(snake_case) : 뱀의 모양을 본다 만든 표기법
		주로 python ...언어 에서 사용된다.

<hr/>

** 예제) a-tag **
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>a태그</title>
</head>
<body>
    <!-- 하이퍼링크를 제공하는 a 태그 -->
     <p>하이퍼링크를 걸어주는 태그:</p> 
    <a href="https://www.naver.com" target="_self">네이버로 이동 (현재 창)</a> 
    <a href="https://www.naver.com" target="_blank">네이버로 이동 (새 탭)</a>
    
</body>
</html>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>a태그</title>
</head>
<body>
    <!-- 하이퍼링크를 제공하는 a 태그 -->
     <p>하이퍼링크를 걸어주는 태그:</p> 
    <a href="https://www.naver.com" target="_self">네이버로 이동 (현재 창)</a> 
    <a href="https://www.naver.com" target="_blank">네이버로 이동 (새 탭)</a>
    
     <!-- target 속성 설명 -->
    <p>target 속성:</p>
    <ul>
        <li><code>_self</code>: 현재 창에서 링크 열기 (기본값)</li>
        <li><code>_blank</code>: 새 탭에서 링크 열기</li>
        <li><code>_parent</code>: 부모 프레임에서 링크 열기 (iframe 사용 시)</li>
        <li><code>_top</code>: 최상위 프레임에서 링크 열기 (iframe 사용 시)</li>
    </ul>

     <!-- 페이지 내 북마크 -->
    <p>페이지 내 북마크:</p>
    <div id="nav">이곳이 북마크 위치입니다.</div>
    <div style="height:1000px;"></div>
    <a href="#nav">맨 위로 이동</a>
</body>
</html>
```





