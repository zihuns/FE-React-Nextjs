# Next.js Movie App

Next.js 14를 사용하여 구축된 영화 정보 애플리케이션입니다.

## 프로젝트 소개

이 프로젝트는 Next.js 14의 최신 기능(App Router, Server Components)을 활용하여 영화 정보를 보여주는 웹 애플리케이션입니다. TypeScript를 사용하여 타입 안정성을 확보하였으며, CSS Modules를 통해 컴포넌트별 스타일링을 적용했습니다.

## 스크린샷

![홈 화면](./screenshot.png)

## 주요 기능

- **영화 상세 정보 조회**: 외부 API를 통해 영화의 포스터, 제목, 평점, 줄거리 등을 가져와 표시합니다 (`components/movie-info.tsx`).
- **서버 사이드 렌더링 (SSR)**: Next.js의 서버 컴포넌트(`async function`)를 활용하여 데이터를 서버에서 미리 가져와 렌더링합니다.
- **Cloudflare Pages 배포**: `@cloudflare/next-on-pages`를 사용하여 Cloudflare Pages 환경에 최적화된 배포 설정을 포함하고 있습니다.

## 기술 스택

- **Framework**: Next.js 14
- **Library**: React 18
- **Language**: TypeScript
- **Styling**: CSS Modules
- **Deployment**: Cloudflare Pages

## 시작하기

### 설치

패키지 의존성을 설치합니다.

```bash
npm install
```

### 개발 서버 실행

개발 모드로 서버를 실행합니다.

```bash
npm run dev
```

브라우저에서 http://localhost:3000으로 접속하여 결과를 확인합니다.
