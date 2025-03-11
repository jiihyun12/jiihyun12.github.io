---
layout: post
title: "programming Day-16"
---

# programming Day-16

[2025-01-21-TUE]

## React



** 예제) useState - checkBox **

```React 
import React, { useState } from 'react';
// 컴포넌트에서 상태 관리를 위해 필요한 훅함수 불러오기

// 함수형 컴포넌트 생성
const CheckValue = () => {
    
    const [message, setMessage] = useState([]);
    // message 값을 업데이트할 수 있는 상태 변수 만들기

// 체크박스 클릭 시 실행될 함수 정의
const onClickToBox = (e) => {
    // 클릭된 체크박스에서 필요한 값 가져오기
    let value = e.target.value;
    // 체크가 되어 있으면 실행할 코드
    if(e.target.checked){
        //상태를 최신 상태로 유지하려면 콜백 함수로 업데이트하는 것이 좋음.
        setMessage((prev)=>[...prev,value]) // 기존 message 배열에 새 값을 추가하여 업데이트하기
        // 콘솔에 출력
    } else{
        // 체크가 해제되었을 때 실행할 코드
        // 현재 message 배열에서 선택 해제된 값을 제거하기
        setMessage(message.filter((data)=>data !== value))
        // 콘솔에 출력
    }
}


return (
        /* 체크박스를 포함한 UI 구성 */
        /* 'Front-end'라는 value 값을 가진 체크박스 생성 */
        /* 'Back-end'라는 value 값을 가진 체크박스 생성 */
        /* 'AI'라는 value 값을 가진 체크박스 생성 */
        /* 선택된 체크박스의 값을 화면에 표시 */
        <div>
            <div>
            <input type="checkBox" value={"Front-end"} onChange={onClickToBox} />  
            {/* input type="checkbox"에서는 onClick보다 onChange가 적절 */}
            {/* onClick을 사용하면 빠르게 연속 클릭할 때 예상치 못한 동작이 발생할 수 있음. */}
            <span>Front-end</span>
            </div>
            <div>
            <input type="checkBox" value={"Back-end"} onChange={onClickToBox} />
            <span>Back-end</span>
            </div>
            <div>
            <input type="checkBox" value={"AI"} onChange={onClickToBox} />
            <span>AI</span>
            </div>
            <h2>{message.join(",")}</h2>
        </div>
    );
};

export default CheckValue;



