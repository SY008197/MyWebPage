# 장상영의 개인 포트폴리오 웹사이트 (MyWebPage)

전북대학교 컴퓨터인공지능학부 장상영의 개인 소개 및 대표 활동 포트폴리오 웹사이트입니다.
- **공개 사이트 URL**: https://sy008197.github.io/MyWebPage/
- **GitHub 저장소 URL**: https://github.com/SY008197/MyWebPage

## 1. 실행 환경 및 로컬 재현 명령 (P56)

### 필요 도구 및 버전
- **Hugo Extended**: `v0.163.0` 이상 (권장 `v0.167.0` 이상)
- **Go**: `v1.20` 이상 (Hugo Modules 테마 의존성 다운로드용)
- **Node.js & npm**: `v20` 이상 (아이콘 및 폰트 의존성 설치용)

### 설치 및 로컬 빌드·실행 절차
저장소를 클론한 뒤 프로젝트 루트 경로에서 아래 명령어를 순서대로 실행합니다.

```bash
# 1. 저장소 클론 및 폴더 이동
git clone https://github.com/SY008197/MyWebPage.git
cd MyWebPage

# 2. npm 패키지 의존성 설치
npm install

# 3. 로컬 개발 서버 실행 (http://localhost:1313/MyWebPage/ 에서 확인)
hugo server

# 4. 정적 파일 빌드 확인 (public/ 폴더에 결과물 생성)
hugo --minify