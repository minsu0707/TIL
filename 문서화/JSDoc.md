# JSDoc으로 React 코드 문서화하기

## JSDoc이란?

**JSDoc은 JavaScript 코드에서 문서를 자동으로 생성하기 위한 주석 표준**이다.  
React 프로젝트에서도 컴포넌트, 함수, 변수의 역할을 명확하게 설명하는 데 사용된다.

- JavaScript 문서 생성기
- HTML, Markdown, JSON 등 다양한 형식 지원
- 주석만으로 문서 자동화 가능

---

## JSDoc 기본 문법

JSDoc은 `/** */` 형태의 주석을 사용한다.

### React 컴포넌트 문서화 예시

```jsx
/**
 * This component renders a greeting to the user.
 *
 * @param {string} name The user's name.
 * @returns {ReactNode} A React element that renders a greeting to the user.
 */
function Greeting({ name }) {
  return <div>Hello, {name}!</div>;
}
```

코드에 JSDoc 주석을 추가한 후, 문서 생성 도구를 사용해 문서를 생성할 수 있다.

---

## JSDoc 문서 생성 도구

- JSDoc (JSDoc3)
- JSDoc to Markdown
- 기타 문서 자동화 도구

---

## React 코드 문서화 원칙

1. 명확하고 간결하게 작성한다
2. 쉬운 표현을 사용한다
3. 불필요한 전문 용어를 피한다
4. 가능한 경우 예제를 제공한다
5. 문서를 항상 최신 상태로 유지한다

---

## React + JSDoc 활용 팁

- 컴포넌트, 함수, 변수의 목적을 문서화한다
- props와 반환 값을 명확히 작성한다
- 코드의 중요한 가정이나 한계를 주석으로 남긴다
- 일관된 주석 스타일을 유지한다

---

## 주요 JSDoc 태그

| 태그 | 설명 |
|------|------|
| `@description` | 컴포넌트, 함수, 변수의 개요 |
| `@param` | 매개변수(Props)의 타입과 설명 |
| `@returns` | 반환 값 설명 |

---

## 요약

- JSDoc은 코드와 문서를 함께 관리하기 위한 도구다
- React 프로젝트에서 유지보수성과 협업 효율을 높여준다
- TypeScript 없이도 명확한 문서화를 할 수 있다
