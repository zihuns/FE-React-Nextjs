# React Warmup

이 프로젝트는 React 학습 및 연습을 위해 구성된 애플리케이션입니다. Create React App을 기반으로 생성되었으며, React Router를 사용한 라우팅과 GitHub Pages를 통한 배포 설정이 포함되어 있습니다.

<img src="public/home.png" alt="Home Screenshot" height="700" />

## 🛠 기술 스택

- **Core**: React (^17.0.2), React DOM (^17.0.2)
- **Routing**: React Router DOM (^5.3.4)
- **Build Tool**: React Scripts (4.0.3)
- **Deployment**: gh-pages (^6.3.0)
- **Type Checking**: Prop-types (^15.8.1)

## 🚀 시작하기

이 프로젝트를 로컬 환경에서 실행하려면 다음 단계를 따르세요.

### 설치

의존성 패키지를 설치합니다.

```bash
npm install
```

### 개발 서버 실행

개발 모드에서 앱을 실행합니다. 브라우저에서 [http://localhost:3000](http://localhost:3000)을 열어 확인할 수 있습니다.

```bash
npm start
```

## 📦 배포 (Deployment)

이 프로젝트는 `gh-pages` 패키지를 사용하여 GitHub Pages에 배포하도록 설정되어 있습니다.

다음 명령어를 실행하면 프로덕션 빌드를 생성하고 GitHub Pages 브랜치로 배포합니다.

```bash
npm run deploy
```

내부적으로 `predeploy` 스크립트가 먼저 실행되어 `npm run build`를 수행한 후 배포가 진행됩니다.
