# web-study

잡다하게 웹 공부한거 올리는 용

## Snake Game - [YouTube 보고함](https://youtu.be/wM7eMJ26kc8 "따라한 영상")  
  

### 새로운 지식  
1. CSS: `repeat(반복횟수, 반복값)`  
    ```css
    display: grid;
    grid-template: repeat(30, 1fr) / repeat(30, 1fr);
    ```
    위 코드처럼 쓰면 *그리드*의 `행`과 `열`을 `1fr`만큼 30개로 나눠 주는거임


    다른 예제 보면
    ```css
    display: grid;
    grid-template-rows: repeat(2, 1fr);         /* 1fr 1fr */
    grid-template-columns: repeat(3, 1fr 2fr);  /* 1fr 2fr 1fr 2fr 1fr 2fr */
    ```
    이렇게 쓰더라고

2. CSS: `calc()`
    ()안의 식을 계산한 결과값을 속성값으로 사용하게 해주는 함수
    ```css
    width: calc(80% - 20px);
    ```
    이러면 80%에서 20px 뺀만큼 설정 해 주더라고

3. Javascript: setInterval(), clearInterval()
    후추


## Snake Game with Vue
숙련도 이슈로 인한 잠정 중단.