# Text AI 사이트

이 레포지토리는 자연어처리(NLP), 텍스트 마이닝, 그리고 BERT 기초에 관한 강의 노트를 제공하는 Jekyll 기반 정적 웹사이트입니다.

## 🚀 로컬 환경 실행 방법 (Local Development)

이 웹사이트는 **Jekyll** 프레임워크와 **Ruby Bundler**를 기반으로 빌드됩니다.

### 1. 사전 요구사항 (Prerequisites)
- [Ruby](https://www.ruby-lang.org/en/downloads/) (버전 2.5 이상 권장, Windows의 경우 [RubyInstaller](https://rubyinstaller.org/) 사용)
- [Node.js](https://nodejs.org/) (NPM 패키지 설치용)

### 2. 의존성 설치 (Install Dependencies)
Ruby 및 Node 의존성을 먼저 구성해야 합니다.
```bash
# Ruby Gem 의존성 설치
bundle install

# NPM 패키지 설치 (선택사항, Bootstrap 등)
npm install
```

### 3. 로컬 서버 실행 (Serve locally)
설치가 완료되면 다음 명령어를 통해 로컬 호스트 테스트 서버를 구동할 수 있습니다. 
기본 포트는 충돌을 피하기 위해 `4001`을 사용하도록 세팅되어 있습니다.

```bash
# 빠른 실행 (NPM Script)
npm start

# 또는 수동 실행
bundle exec jekyll serve --port 4001
```

로컬 서버 구동 후 브라우저에서 `http://127.0.0.1:4001/` 로 접속할 수 있습니다.

## 📦 정적 웹페이지 빌드 옵션 (Build Settings)
정적 파일 산출물은 기본적으로 `docs/` 리포지토리에 생성되도록 `_config.yml`의 `destination` 옵션에 지정되어 있습니다. (GitHub Pages 배포 지원)

```bash
# 빌드 폴더 생성
npm run build 
# 혹은 bundle exec jekyll build
```

## 🛠️ 사이트 구조
- `src/` : 실제 편집되는 마크다운(`md`) 소스코드와 `CNAME`, 정적 자산(assets)이 들어 있습니다.
- `docs/` : Jekyll이 렌더링한 최종 `.html` 산출물이 저장되는 위치입니다.
- `_layouts`, `_includes`, `_sass` : 프론트엔드 UI 디자인과 레이아웃 템플릿입니다.
- `_data/` : 상단 및 메인 네비게이션 트리 데이터(`.yml`) 경로입니다.
