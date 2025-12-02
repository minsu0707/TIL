# Orval

Orval은 OpenAPI v3 / Swagger v2의 YAML 또는 JSON 스펙을 기반으로, 타입이 안전한 TypeScript 모델과 HTTP 요청 함수를 자동으로 생성해주는 도구입니다.  

기본 HTTP 클라이언트는 **Axios**를 사용하지만, 프로젝트에 맞게 다른 클라이언트로도 변경 가능합니다.  

주요 프레임워크와 호환됩니다:
- Angular
- React
- Vue

## 핵심 동기
기존 Swagger Editor/Codegen만으로는 현대 개발 요구를 충족하기 어렵습니다. Orval은 이러한 한계를 보완합니다.

## 주요 기능
- 타입 안전한 **TypeScript 모델 생성**
- **HTTP 요청 함수 생성**
- **MSW(Mock Service Worker)를 이용한 mock 데이터 생성**
- **React Query + Axios** 통합 생성
- **Angular + HttpClient** 통합 생성
