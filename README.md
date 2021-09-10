# TIL-JAVASCRIPT
[Today I Learn] javascript 공부

## 0908 ~ 0910

<details>
  <summary>javascript basic</summary>
  
### javascript basic


  
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
                                
---

### 자바스크립트 내장 함수 
#### String
  * indexOf - 문자열이 시작하는 시점의 index번호 / 찾지못하면 -1
  * lastIndexOf - 뒤
  * slice(시작점,끝점) - 시작점부터 끝점 문자열만
  * substr(시작점,시작점으로부터 글자수) - 글자수
  * replace(원래값,바꿀값) - 바꾸기
  * uppercase - 대,소문자로 변환
    * toLocaleUpperCase
    * toLowerCase
  * concat - var txt4 = txt1.concat(" ",txt2); 문자열 합치기.
  * trim - 앞,뒤 공백제거
  * padStart - (만들 글자수,넣어줄 값) ex)날짜 자리수 맞춰줄때 01,02,03,...,11,12
  * padEnd
  * charAt - 문자열에서 (자리수)만큼의 특정 값을 호출
  * split() - ()기준으로 자르고 배열로 나눔.
    * var tags = "키보드,기계식,블루투스,맥마우스";
    * var arr = tags.split(",");
    * arr = {0: "키보드" 1: "기계식" 2: "블루투스" 3: "맥마우스"};
#### Number
  * toString(); - 숫자를 문자열로 변환
  * toFixed() - 지정된 소수점 자리수까지 반올림으로 표기
  * toPrecision() - 정수까지 포함 한 자리수
  * parseInt() - 무조건 정수 = 소수점부터 무시
  * parseFloat() - 소수점까지 표기
#### Boolean
  * 이건 true or false
    * false : undifined / null / 0 / -0 / NaN / ""(빈문자열)
#### Array
  * toString()
  * join() - 배열 사이에 ()값이 삽입
  * document.getElementById("div1").innerHTML = txt;
  * pop() - 배열의 가장 마지막 element를 제거 후 리턴 해줌.
  * push() - 배열의 마지막에 새로운 element를 추가
  * shift() - 배열의 첫번째 element를 제거 후 리턴 해줌.
  * unshift() - 배열의 첫번째에 새로운 element를 추가
  * splice(1,2,3,4) : 배열 / 파라미터 1 : 시작위치 / 파라미터 2 : 삭제할 element 수 / 1,2까지만 넣을시 삭제만 함 / 파라미터 3 : 시작위치 / 파라미터 4 : 시작위치
  * concat() - 합침
  * slice(시작,종료) - 배열 시작+1부터 종료까지
  * sort() - 오름차순,내림차순 return a.point > b.point ? -1 : a.point < b.point ? 1 : 0;
  * filter - return person.city == "제주"; city가 "제주"로 되어있느사람만 !필터!
  * reduce(누적값, 현잿값, 인덱스, 요소) - 누적값
  * map(요소, 인덱스, 배열) - 배열안의 요소들을 짝지어줌
  다시공부
#### Date
  * getTimezoneOffset - 분단위, GMT +0기준으로 분차를 알려줌
    * Time zone 글로벌 서비스시 GMT +0 기준으로 저장(한국:GMT +0900)
#### Math
  * round() - 반올림
  * ceil() - 무조건 올림으로 정수를 만듬. 페이징할때 사용 가능
  * floor() - 소수점 이하는 무조건 내림
  * trunc() - 정수부분만 리턴
  * sign() - 음수이면 -1, 양수이면 1, 0이면 0
  * pow() - 제곱
  * sqrt() - 루트
  * abs() - 무조건 양수로 변환
  * max()
  * min()
  * random() - 랜덤..
#### JSON
#### Window
#### 크롬개발자도구
                                                                        
---
                                                                        
## 0910
### 자바스크립트 고급 문법
#### this 키워드
#### Scope
#### Default Function Parameter                                                                        
#### Default Function Parameter                                                                        
#### Arrow Function
#### Template Literals                                                                       
#### Object Literal Syntax Extension
#### Spread Operator                                                                        
#### Object Destructuring                                                                        
#### Array Destructuring                                                                        
#### Promise
#### Async/Await                                                                         
#### 모듈(Module)
#### 클래스(Class)                                                                        
#### Error - try/catch/finally                                                                        
#### Strict Mode                                                                        
#### 정규식(RegExp)
#### HTML Element 컨트롤                                                                        
#### HTML 이벤트 컨트롤
#### HTML 스타일 컨트롤                                                                        
#### 데이터테이블 만들기                                                                        
                                                                      
                                                                   
                                                                    
  
</details>
