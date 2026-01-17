# React Bookshelf

개인 서재 관리 애플리케이션입니다. 책 목록을 조회하고, 새로운 책을 추가하며, 책 정보를 관리할 수 있습니다.

![screenshot](./public/app.png)

## 📋 프로젝트 소개

React와 TypeScript로 개발된 SPA(Single Page Application)로, 사용자 인증을 통해 개인 서재의 책들을 관리할 수 있습니다.

## 🛠 기술 스택

- **Frontend Framework**: React 18
- **Language**: TypeScript
- **State Management**: Redux, Redux Saga
- **Routing**: React Router v5, Connected React Router
- **UI Library**: Ant Design
- **HTTP Client**: Axios
- **Build Tool**: Create React App

## 📁 프로젝트 구조

```
react-bookshelf/
├── public/                 # 정적 파일
├── src/
│   ├── components/         # 프레젠테이션 컴포넌트
│   │   ├── Add.tsx
│   │   ├── Book.tsx
│   │   ├── Layout.tsx
│   │   ├── List.tsx
│   │   └── Signin.tsx
│   ├── containers/         # 컨테이너 컴포넌트 (Redux 연동)
│   │   ├── AddContainer.tsx
│   │   ├── ListContainer.tsx
│   │   └── SigninContainer.tsx
│   ├── pages/              # 라우트 페이지 컴포넌트
│   │   ├── Home.tsx
│   │   ├── Add.tsx
│   │   ├── Detail.tsx
│   │   ├── Edit.tsx
│   │   ├── Signin.tsx
│   │   ├── NotFound.tsx
│   │   └── Error.tsx
│   ├── redux/              # Redux 상태 관리
│   │   ├── modules/
│   │   │   ├── auth.ts      # 인증 모듈
│   │   │   ├── books.ts     # 책 관리 모듈
│   │   │   ├── reducer.ts   # 루트 리듀서
│   │   │   └── rootSaga.ts  # 루트 사가
│   │   └── create.ts        # Redux 스토어 생성
│   ├── services/           # API 서비스
│   │   ├── BookService.ts
│   │   ├── UserService.ts
│   │   └── TokenService.ts
│   ├── hooks/              # 커스텀 훅
│   │   └── useToken.ts
│   ├── types.ts            # TypeScript 타입 정의
│   ├── history.ts          # 라우터 히스토리
│   └── App.tsx             # 메인 앱 컴포넌트
└── package.json
```

## ✨ 주요 기능

### 🔐 사용자 인증
- 이메일/비밀번호 기반 로그인
- JWT 토큰 기반 인증
- 로컬스토리지를 통한 토큰 관리
- 인증되지 않은 사용자는 자동으로 로그인 페이지로 리다이렉트

### 📚 책 관리
- **조회**: 등록된 모든 책 목록 확인
- **추가**: 새로운 책 정보 추가 (제목, 저자, URL 등)
- **삭제**: 등록된 책 삭제
- **상세**: 개별 책 상세 정보 확인
- **편집**: 책 정보 수정

### 🎨 사용자 인터페이스
- Ant Design 컴포넌트 활용
- 반응형 레이아웃
- 에러 바운더리를 통한 에러 처리

## 🚀 시작하기

### 사전 요구사항

- Node.js (v14 이상 권장)
- npm 또는 yarn

### 설치

```bash
# 의존성 패키지 설치
npm install
```

### 실행

```bash
# 개발 서버 실행
npm start
```

브라우저에서 [http://localhost:3000](http://localhost:3000)을 열어 확인하세요.

### 빌드

```bash
# 프로덕션 빌드
npm run build
```

### 테스트

```bash
# 테스트 실행
npm test
```

## 📡 API 연동

이 프로젝트는 다음 API를 사용합니다:
- **Base URL**: `https://api.marktube.tv/v1`
- **인증**: Bearer Token 방식
- **Endpoints**:
  - `POST /me` - 로그인
  - `DELETE /me` - 로그아웃
  - `GET /book` - 책 목록 조회
  - `POST /book` - 책 추가
  - `DELETE /book/:id` - 책 삭제

## 🏗 아키텍처

### 상태 관리

Redux와 Redux Saga를 사용하여 비동기 작업과 상태를 관리합니다:

- **Auth Module**: 사용자 인증 상태 관리
- **Books Module**: 책 목록 및 CRUD 작업 관리

### 컴포넌트 구조

- **Container Pattern**: 프레젠테이션 컴포넌트와 컨테이너 컴포넌트를 분리
- **Custom Hooks**: 재사용 가능한 로직을 훅으로 추출 (예: `useToken`)

### 라우팅

- React Router를 사용한 클라이언트 사이드 라우팅
- Connected React Router로 Redux와 라우터 연동

## 📝 라이센스

이 프로젝트는 개인 학습 및 포트폴리오 목적으로 작성되었습니다.
