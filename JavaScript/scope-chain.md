# 스코프 체인
## 스코프
식별자에 대한 유효 범위.

## 스코프 체인
전역공간을 제외하면 **오직 함수에 의해서만** 스코프가 생겨난다.
*식별자의 유효범위*를 안에서부터 바깥으로 차례로 검색해나가는 것을 스코프 체인이라 한다. 이것을 가능하게 하는 것이 LexicalEnvironment의 outerEnvironmentReference 이다.


### 변수 은닉화 (variable shadowing)
현재 실행 컨텍스트에서 a 라는 변수가 있다면, 외부 컨텍스트의 동일한 이름의 a 변수에는 접근할 수 없다.

(...ing)