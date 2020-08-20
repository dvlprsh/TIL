# JavaScript Array method 정리
- [Array.prototype.concat](#Array.prototype.concat())
- [Array.prototype.reduce](#Array.prototype.reduce())
- [Array.prototype.some](#Array.prototype.some())
## Array.prototype.concat()
**concat()** 메서드는 인자로 주어진 배열이나 값들을 기존 배열에 합쳐서 새 배열을 반환합니다.
> 참고: 배열이나 값을 이어붙여도 원본은 변하지 않으며, 새로운 배열이나 원본 배열을 조작해도 서로 영향을 받지 않습니다.
### 구문
```javascript
array.concat([value1[, value2[, ...[, valueN]]]])
```
#### 매개변수
- 배열 또는 값
- 만약 value1 ~ valueN 인자를 생략하면 기존 배열의 얕은 복사본을 반환
#### 반환값
새로운 **Array** 객체

### Examples
```javascript
const array1 = ['a', 'b', 'c']
const array2 = ['d', 'e', 'f']
const array3 = array1.concat(array2)

console.log(array3);
// expected output: Array ["a", "b", "c", "d", "e", "f"]
```

```javascript
const alpha = ['a', 'b', 'c'];
const numeric = [1, 2, 3];

alpha.concat(numeric);
// result: ['a', 'b', 'c', 1, 2, 3]
```

```javascript
const num1 = [1, 2, 3];
const num2 = [4, 5, 6];
const num3 = [7, 8, 9];

num1.concat(num2, num3);
// result: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

```javascript
const alpha = ['a', 'b', 'c'];

alpha.concat(1, [2, 3]);
// result: ['a', 'b', 'c', 1, 2, 3]
```

## Array.prototype.reduce()
**reduce()** 메서드는 배열의 각 요소에 대해 주어진 *리듀서(reducer)* 함수를 실행하고, 하나의 결과값을 반환합니다.

#### 매개변수
- callback
  * accumulator


## Array.prototype.some()
---
### 출처
concat
- https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/concat