# 장상영의 개인 포트폴리오 웹사이트 (MyWebPage)

전북대학교 컴퓨터인공지능학부 장상영의 개인 소개 및 대표 활동 포트폴리오 웹사이트입니다.
- **공개 사이트 URL**: https://sy008197.github.io/MyWebPage/
- **GitHub 저장소 URL**: https://github.com/SY008197/MyWebPage

  ## 1. 실행 환경 및 로컬 재현 명령 
    ### 필요 도구 및 버전
    - **Hugo Extended**: `v0.163.0` 이상 (권장 `v0.167.0` 이상)
    - **Go**: `v1.20` 이상 (Hugo Modules 테마 의존성 다운로드용)
    - **Node.js & npm**: `v20` 이상 (아이콘 및 폰트 의존성 설치용)

    ### 설치 및 로컬 빌드·실행 절차
    저장소를 클론한 뒤 프로젝트 루트 경로에서 아래 명령어를 순서대로 실행합니다.

    ```bash
    git clone https://github.com/SY008197/MyWebPage.git
    cd MyWebPage

    npm install

    hugo server

    hugo --minify


## 2. 콘텐츠 수정 및 자동 재배포 안내 

  ### 주요 수정 파일 위치 (저장소 루트 기준 상대 경로)
  - **기본 프로필 및 첫 화면 타이핑 문구**: `data/ko/author.yaml`, `data/en/author.yaml`
  - **사이트 메타데이터 및 OpenGraph 설정**: `data/ko/site.yaml`, `data/en/site.yaml`, `hugo.yaml`
  - **소개(`#about`) 및 학습 목표**: `data/ko/sections/about.yaml`, `data/en/sections/about.yaml`, `layouts/partials/sections/about.html`
  - **역량(`#skills`) 및 적용 사례**: `data/ko/sections/skills.yaml`, `data/en/sections/skills.yaml`, `layouts/partials/cards/skill.html`
  - **대표 활동(`#experiences`)**: `data/ko/sections/experiences.yaml`, `data/en/sections/experiences.yaml`
  - **프로필·배경·로고 이미지 자산**: `assets/images/author/john.png`, `assets/images/site/background.jpg`, `assets/images/site/main-logo.png`, `assets/images/site/inverted-logo.png`, `assets/images/site/favicon.png`

  ### 수정 후 배포 및 공개 화면 확인 방법
  1. 위 경로의 파일들을 수정합니다.
  2. `main` 브랜치에 변경 사항을 커밋하고 원격 저장소에 푸시합니다.

      git add .
      git commit -m "수정 내용 요약"
      git push origin main

  3. `main` 브랜치에 `push`가 발생하면 `.github/workflows/hugo-pages.yml` 워크플로가 자동 실행됩니다.
  4. GitHub Actions 탭(`https://github.com/SY008197/MyWebPage/actions`)에서 `Deploy Hugo to GitHub Pages` 워크플로가 초록색(`Success`)으로 완료되었는지 확인합니다.
  5. 시크릿 창(비로그인 상태)에서 공개 사이트 주소(`https://sy008197.github.io/MyWebPage/`)에 접속하여 변경 사항이 반영되었는지 확인합니다.
