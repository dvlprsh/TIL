# 실행 컨텍스트 (Execution Context)
## 실행 컨텍스트
실행할 코드에 제공할 환경 정보들을 모아놓은 객체.
주로 함수에 의해서 실행됨.
실행 컨텍스트 객체는 활성화 되는 시점에 VariableEnvironment, LexicalEnvironment, ThisBinding의 세 가지 정보를 수집한다.
>An execution context is a specification device that is used to track the runtime evaluation of code by an ECMAScript implementation.  
[ecma-262](http://www.ecma-international.org/ecma-262/6.0/index.html#sec-execution-contexts)
### 실행 컨텍스트 내부 정보
- VariableEnvironment  
    현재 컨텍스트 내의 식별자들에 대한 정보 + 외부 환경 정보.
    선언 시점의 LexicalEnvironment의 스냅샷(snapshot)으로, 변경 사항은 반영되지 않음.
- LexicalEnvironment  
    처음에는 VariableEnvironment와 같지만 변경 사항이 실시간으로 반영됨.
- ThisBinding  
    식별자가 바라봐야 할 대상 객체. this로 지정된 객체가 저장됨.

#### VariableEnvironment
VariableEnvironment에 담기는 내용은 LexicalEnvironment와 같지만 최초 실행 시의 스냅샷을 유지한다는 점이 다르다.

### 실행 컨텍스트 생성 과정
1. VariableEnvironment에 먼저 정보를 담는다.
2. 이를 그대로 복사해서 LexicalEnvironment를 생성한다.
3. 이후에는 LexicalEnvironment를 주로 활용한다.

[참고](http://dmitrysoshnikov.com/ecmascript/es5-chapter-3-2-lexical-environments-ecmascript-implementation/)

VariableEnvironment와 LexicalEnvironment 내부는 **environmentRecord** 와 **outerEnvironment** 로 구성되어 있다.

(...ing)

---
### 참고
-  코어 자바스크립트
- http://dmitrysoshnikov.com/ecmascript/es5-chapter-3-2-lexical-environments-ecmascript-implementation/
- http://www.ecma-international.org/ecma-262/6.0/index.html#sec-execution-contexts