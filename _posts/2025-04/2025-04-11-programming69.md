---
layout: post
title: "programming Day-69"
---

# programming Day-69

[2025-04-11-FRI]


컨트롤러에서 서비스 로직이 다 만들어지기떄문에 가장 중요!


flsh 영역을 사용할 수 있을 때
1. 로그인 실패
2. 인증 ...




========================================================================

mapper - interfece - DAO - service - Controller


3-tier
   스프링 프로젝트는 3-tier 방식으로 구성한다.

   [Presentation Tier - 화면 계층]
      화면에 보여주는 기술을 사용하는 영역.
      컨트롤러에서 사용자의 요청에 맞는 응답처리를 진행하며,
      HTML엔진(Thymeleaf), HTML등이 담당하는 영역이다.
      화면 구성이 이에 속한다.

   [Business Tier - 비지니스 계층]
      순수한 비지니스 로직을 담고 있는 영역.
      고객이 원하는 요구사항을 반영하는 계층이기 때문에 서비스에 있어서 가장 중요한 영역이다.
      이 영역의 설계는 고객의 요구 사항과 정확히 일치해야 하며, 서비스 영역이다.

   [Persistence Tier - 영속 계층 혹은 데이터 계층]
      데이터를 어떤 방식으로 보관하고, 사용하는 가에 대한 설계가 들어가는 계층.
      일반적으로 DBMS를 많이 이용하지만, 상황에 따라서 네트워크 호출 혹은 원격 호출 등의 기술이 접목될 수 있다.

각 영역은 독립적으로 설계되어 나중에 특정한 기술이 변하더라도 필요한 부분을 전자제품의 부품처럼
쉽게 교환할 수 있게 하자는 방식이다. 각 연결 부위는 인터페이스를 이용해서 설계하는 것이 일반적인 구성 방식이다.
----------------------------------------------------------------------------------------------------------------------------------
               Presentation ↔ Business ↔ Persistence ↔ DBMS
                       ↑         ↑              ↑
                  Controller    Service          Mapper
----------------------------------------------------------------------------------------------------------------------------------
비지니스 계층
   프레젠테이션 계층과 영속 계층의 중간 다리 역할을 한다.
   영속 계층은 DBMS를 기준으로, 비지니스 계층은 로직을 기준으로 처리한다.
   예를 들어 쇼핑몰에서 상품 구매시 포인트 적립을 한다고 가정한다면,
   영속 계층의 설계는 '상품', '회원'으로 나누어 설계하지만 비지니스 계층은
   상품 영역과 회원 영역을 동시에 사용해서 하나의 로직을 처리하게 된다.
   이 때 하나의 서비스에 필요한 여러 개의 쿼리 메소드를 하나로 묶어주는 역할이 필요한데, 
   이를 Service 객체로 사용한다.





persistance tier
servist Teyt
preseentario


MemberService 누르고 ctrl 엔터 눌러서 implements 생성한다.
임플리먼츠에서 오버라이드 만들떄 p누른다








