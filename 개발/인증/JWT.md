### JWT란?

- JSON (JSON Web Token)은 웹에서 인증정보를 안전하게 전송하기 위한 토큰

간추리면

- 로그인 후 서버가 주는 “출입증” 같은 것
- 이 출입증으로 “나 로그인한 사람이야”라고 증명

## JWT구조

```tsx
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjEsImVtYWlsIjoidGVzdEB0ZXN0LmNvbSJ9.abc123def456
```

→ 대충 이렇게 생김

- 점으로 3부분을 나눔
1. 헤더: 토큰 타입, 암호화 방식
2. 페이로드: 사용자 정보(userId, email 같은 거)
3. 서명: 토큰이 변조되지 않았음을 증명

## JWT 왜 사용하나?

기존 방식(세션)

```tsx
로그인 -> 서버에 세션 저장 -> 세션 ID를 쿠키로 전송
```

jwt방식

```tsx
로그인 -> JWT 토큰 생성 -> 토큰을 클라이언트에 전송
```

장점

- 서버 부담이 줄어듬: 세션을 서버에 저장할 필요가 없음
- 확장성 좋음: 여러 서버에서 토큰 검증 가능