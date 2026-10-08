# 캐시페이 (CashPay)

콘텐츠이용료 현금화 안내 웹사이트.  
프론트는 **Next.js(Node.js)**, API는 **Spring Boot(Java)** 로 구성합니다.

## 구조

```
cashpay/
  frontend/   Next.js 메인·키워드 페이지 (SEO SSR)
  backend/    Spring Boot API (헬스체크 골격)
```

## 프론트엔드 실행

Node.js 18+ 필요. 로컬에 Node가 없다면 프로젝트의 `.tools/node`를 PATH에 추가해도 됩니다.

```bash
cd frontend
npm run dev
```

브라우저: http://localhost:3000

## 백엔드 실행

JDK 17+ / Maven 필요.

```bash
cd backend
mvn spring-boot:run
```

헬스체크: http://localhost:8080/api/health

## SEO 적용 메모 (메인)

- 메인 H1·메타는 `콘텐츠이용료 현금화` 허브에 집중
- 정보이용료 / 소액결제 / 상품권은 별도 URL로 분리 (현재 플레이스홀더)
- FAQ·Organization JSON-LD 포함
- 연락처·도메인·사업자 정보는 `frontend/src/lib/site.ts`에서 교체
