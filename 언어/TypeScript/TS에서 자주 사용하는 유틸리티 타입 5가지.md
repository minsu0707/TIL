1. **`Partial<T>`**
- 설명: 주어진 타입 `T`의 모든 프로퍼티를 optional로 만듭니다.
- 예시:

```tsx
type User = { name: string; age: number };
type PartialUser = Partial<User>; // { name?: string; age?: number }
```

2. **`Required<T>`**
- 설명: 주어진 타입 `T`의 모든 프로퍼티를 필수로 만듭니다.
- 예시:

```tsx
type User = { name?: string; age?: number };
type RequiredUser = Required<User>; // { name: string; age: number }
```

3. **`Readonly<T>`**
- 설명: 타입 `T`의 모든 프로퍼티를 읽기 전용으로 만듭니다. 수정 불가.
- 예시:

```tsx
type User = { name: string; age: number };
type ReadonlyUser = Readonly<User>;
const user: ReadonlyUser = { name: "John", age: 30 };
user.age = 31; // ❌ 오류
```

4. **`Pick<T, K>`**
- 설명: 타입 `T`에서 특정 프로퍼티 `K`만 선택해서 새 타입을 만듭니다.
- 예시:

```tsx
type User = { name: string; age: number; email: string };
type UserNameAndEmail = Pick<User, "name" | "email">; // { name: string; email: string }
```

5. **`Omit<T, K>`**
- 설명: 타입 `T`에서 특정 프로퍼티 `K`를 제외한 새 타입을 만듭니다.
- 예시:

```tsx
type User = { name: string; age: number; email: string };
type UserWithoutEmail = Omit<User, "email">; // { name: string; age: number }
```