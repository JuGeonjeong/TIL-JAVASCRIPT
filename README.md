# TIL-JAVASCRIPT
[Today I Learn] javascript 공부

## 0908 ~ 0909
### javascript basic

<details>
  
#### 자바스크립트 작성위치
#### 콘솔
#### 주석처리
#### 변수 선언자(var, let, const)
  * var = 재선언 가능, 거의 안씀.  
  * let = 선언된 변수에 값의 재할당이 가능하지만 같은변수명으로 재선언불가.   
  * const = 절대값, 재선언 재할당 불가.  
#### 데이터 타입
  * String.  
  * Number - '', "" 없이 사용가능.   
  * Undifined - 선언되지않음. 하나의 데이터 타입.   
  * Null - 할당 값이 준비되지 않았을 때. 넣어서 쓰임.   
  * Object - 여러속성을 하나의 변수에 저장 할 수 있도록 해주는 데이터 타입. key:value.  
  * Array - 배열   
  * Boolean - true / false   
  * typeof x - x가 어떤 유형인지 알려줌.   
#### 64비트 부동소수점
  * toString(2) - 2진수로 표현
    * 1비트 - 양수 0, 음수 1
    * 11비트 - 지수부 - 2^(n-1)-1 + m
    * 52비트 - 가수부 - 
    * 2^10 = 1024 - 1 - 4 = 1019
    * 무한소수인경우 64비트를 넘어갔을때, 가장가까운 숫자로 표현 = 외부라이브러리 사용
      * BigNumber.js
      * Big.js
      * Decimal.js
  뭔소리인지 몰라서 이해못함.
#### 연산자
  * 더하기, 빼기, 곱하기, 나누기, 거듭제곱(**), 나머지(%), 1씩증가(++), 1씩감소(--)
  * 문자열 연산자 
    * txt1 += txt2; //txt1 = txt1 + txt2;
    * 숫자 + 문자 = 문자
  * 비교 연산자
    * (x == y) - equal to
    * (x == "y") - 비교연산자로 들어가면 "" 안에 값만 봄
    * (x === y) - 데이터 타입으로 비교
    * !=, !==, !===
  * Logical 연산자
    * && - and
    * || - or
    * ! - console.log(!(3 < 2)); 조건값을 반대로 해줌
#### 조건문(if, switch
  * if(조건) else if(조건) else
  * switch(조건) case(조건값) break;빠져나옴                        
#### 반복문(for, for-in, for-of, while)
  * for(조건) {코드}; - 조건이 만족하는 동안에 계속해서 {}안의 코드를 실행.
    * for - in : for(var i in numbers){console.log(numbers[i];} - numbers안 전부 출력.
    * for - of : for(var num of numbers){console.log(num);} - in이랑 뭐가 다른지 모르겠음.
  * while(조건){} : 뭐라 정리를.... ! for랑 차이를 내일 봐야겠다.
    * do-while(조건){} : while조건 안보고 do먼저 실행
#### 함수
  * function name() {} - 특정 기능을 수행하도록 작성된 코드 블럭. 잘 짜놓으면 좋음.                             
  
</details>

---

### 자바스크립트 내장 함수 

<details>
  
#### String 
#### Number
#### Boolean
#### Array
#### Date
#### Math
#### JSON
#### Window
#### 크롬개발자도구
  
</details>
