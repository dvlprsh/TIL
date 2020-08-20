# undefined / null / empty
JavaScript에 '없음'을 나타내는 두 가지 값이 있다.
- undefined
- null  
두 값의 의미와 사용하는 목적이 다르다.

## undefined 가 사용되는 경우
1. 사용자가 명시적으로 undefined를 값으로 지정하는 경우  
    -> undefined 그 자체로 **하나의 값**으로 동작한다.  
    이 때 undefined 가 할당된 프로퍼티나 배열의 요소는 고유의 키값(프로퍼티 이름)이 실존하게 되고, 배열 순회 시 순회의 대상이 된다.
2. 값이 존재하지 않을 때 **자바스크립트 엔진**이 자동으로 부여하는 경우
    - 값을 대입하지 않은 변수. 즉, 값에 메모리 주소를 지정하지 않은 식별자에 접근할 때
    - 객체 내부의 존재하지 않는 프로퍼티에 접근하려고 할 때
    - return 문이 없거나 호출되지 않는 함수의 실행 결과

## empty (...ing)

```javascript
var arr1 = [undefined, 1];
var arr2 = [];
arr2[1] = 1;

arr1.forEach(function(v, i) { console.log(v, i); });

```
    
---
### 출처
- 코어 자바스크립트 p.29~30