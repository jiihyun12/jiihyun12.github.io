---
layout: post
title: "programming Day-04"
---

# programming Day-04

[2025-01-03]

## `width`를 지정하는 방법

1. **`px`**: 절대적인 크기.
2. **`%`**: 부모 요소의 크기를 기준으로 하는 상대적인 크기.  
   - 단, 부모 요소의 크기가 지정되어 있지 않으면 브라우저 크기를 상속받는다.
3. **`vw`, `vh`, `dvw`, `dvh`**: 브라우저 크기를 기준으로 하는 상대적인 크기.
   - `vw`: 뷰포트 너비의 1%.  
   - `vh`: 뷰포트 높이의 1%.  
   - `dvw`, `dvh`: 브라우저의 동적 뷰포트 너비와 높이.
	
---

## 디스플레이 `flex`

- **Flexible Box (Flexbox)**:  
  - 요소의 크기와 순서를 유연하게 조정하며, 한 줄에 요소를 배치하는 속성.  
  - 단, 요소의 크기보다 브라우저의 크기가 작아지면 한 줄에 꽉 차 보이도록 크기를 조정한다.

---

### Flexbox 주요 속성

1. **`flex-direction`**
   - Flex container가 자식을 어떻게 배치할지 정하는 속성.  
   - 메인 축(Main Axis)의 방향을 설정.
     - `row` (기본값): 가로 방향.
     - `row-reverse`: 가로 방향 반대로 정렬.
     - `column`: 세로 방향.
     - `column-reverse`: 세로 방향 반대로 정렬.

2. **`justify-content`**
   - 메인 축의 정렬 방식을 설정.  
     - 주요 값:
       - `flex-start`: 요소들을 시작점에 정렬.
       - `flex-end`: 요소들을 끝점에 정렬.
       - `center`: 요소들을 중앙에 정렬.
       - `space-between`: 요소들 사이를 동일한 간격으로 배치.
       - `space-around`: 요소들 사이 및 양끝에 동일한 간격 배치.
       - `space-evenly`: 요소들 사이를 동일한 간격으로 고르게 배치.

3. **`align-items`**
   - 반대 축(Cross Axis)의 정렬 방식을 설정.  
     - 주요 값:
       - `stretch` (기본값): 요소를 축 방향으로 늘린다.
       - `flex-start`: 요소들을 시작점에 정렬.
       - `flex-end`: 요소들을 끝점에 정렬.
       - `center`: 요소들을 중앙에 정렬.
       - `baseline`: 텍스트의 기준선에 맞춰 정렬.

4. **`flex-wrap`**
   - Flex container의 자식 요소가 부모 크기보다 커졌을 때(넘칠 때) 처리 방식을 설정.
     - 주요 값:
       - `nowrap` (기본값): 요소들을 한 줄에 배치.
       - `wrap`: 요소들을 여러 줄에 배치.
       - `wrap-reverse`: 요소들을 역방향으로 여러 줄에 배치.

5. **`align-self`**
   - 개별 자식 요소의 위치를 설정하는 속성.  
     - 값은 `align-items`와 동일하지만, 특정 요소에만 적용.

---

### Flexbox의 특징

1. 자식 요소는 기본적으로 자신이 가진 내용물의 `width`만큼 차지한다.
2. `width`, `height`를 지정할 수 있다. (이는 `inline-block` 속성과 유사하다.)
	
