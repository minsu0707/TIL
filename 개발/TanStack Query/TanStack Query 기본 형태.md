## TanStack Query

1. 데이터 가져오기 (GET) - useQuery

```tsx
import { useQuery } from "@tanstack/react-query"

const { data, error, isLoading } = useQuery({
	queryKey: ['users'],
	queryFn: ( => fetch('/api/users').then(res => res.json()),
	staleTime: 1000 * 60,
});
```

- data → 서버에서 가져온 데이터
- error → 에러 정보
- isLoading → 로딩 상태

1. 데이터 변경 (POST/PUT/DELETE) - useMutation

```tsx
import { useMutation, useQueryClient } from '@tanstack/react-query'

const queryClient = useQueryClient();

const mutation = useMutation({
	mutationFn: (newUser) => 
		fetch('/api/users', {
			method: 'POST',
			body: JSON.stringify(newUser,)
		}),
	onSuccess: ( => queryClient.invalidateQueries(['users'])), // 캐시 갱신
});
```

- mutation.mutate(user) → 서버로 데이터 전송
- 성공 시 관련 캐시를 무효화(invalidate)하여 최신화

## 핵심 포인트

- GET → useQuery, 캐싱/자동 갱신 지원,
- POST/PUT/DELETE → useMutation, 캐시 무효화 관리
- 캐시는 queryKey 기준으로 메모리에 저장