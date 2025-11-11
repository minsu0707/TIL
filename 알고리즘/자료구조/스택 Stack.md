# 스택(Stack) 자료구조

## 1. 정의
스택은 **후입선출(Last In First Out, LIFO)** 방식으로 데이터를 저장하는 자료구조입니다.  
즉, **가장 나중에 들어간 데이터가 가장 먼저 나옵니다**.

입력 순서: A → B → C
출력 순서: C → B → A


---

## 2. 특징
- 한쪽 끝(Top)에서만 **삽입(push)과 삭제(pop)** 가능
- 데이터를 순차적으로 접근해야 함
- 구현 방법
  - 배열(Array)
  - 연결 리스트(Linked List)

---

## 3. 기본 연산
| 연산 | 설명 |
|------|------|
| `push(value)` | 스택의 맨 위에 데이터를 추가 |
| `pop()` | 스택의 맨 위 데이터를 제거하고 반환 |
| `peek()` / `top()` | 스택의 맨 위 데이터를 확인 (삭제하지 않음) |
| `isEmpty()` | 스택이 비어있는지 확인 |
| `size()` | 스택에 있는 데이터 개수 반환 |

---

## 4. 장단점

### 장점
- 구현이 간단
- 최근 데이터를 우선적으로 처리할 때 유용 (예: 함수 호출, 뒤로가기 기능)

### 단점
- 원하는 위치의 데이터를 직접 접근 불가
- 메모리 한정적일 수 있음 (배열 기반 스택)

---

## 5. 사용 예시
- 웹 브라우저 **뒤로가기 / 앞으로가기**
- **함수 호출 스택(Call Stack)**
- **수식 계산**, **괄호 검사**
- Undo / Redo 기능

---

## 6. 예제 (JavaScript)
```javascript
class Stack {
  constructor() {
    this.items = [];
  }

  push(element) {
    this.items.push(element);
  }

  pop() {
    if (this.isEmpty()) return null;
    return this.items.pop();
  }

  peek() {
    if (this.isEmpty()) return null;
    return this.items[this.items.length - 1];
  }

  isEmpty() {
    return this.items.length === 0;
  }

  size() {
    return this.items.length;
  }
}

// 사용 예시
const stack = new Stack();
stack.push(1);
stack.push(2);
console.log(stack.peek()); // 2
console.log(stack.pop());  // 2
console.log(stack.isEmpty()); // false
