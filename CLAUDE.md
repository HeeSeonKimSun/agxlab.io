# CLAUDE.md — AGX Lab website

이 리포는 al-folio v1.x 스타터로 만든 **연구실 사이트**(agxlab.io)입니다. 런타임(레이아웃·SCSS·플러그인)은 gem(`al_folio_core` 등)에 있고, 이 리포에는 내용과 설정, 그리고 몇 개의 로컬 오버라이드만 있습니다.

## 어디를 고치나

- 내용: `_pages/` (about=홈, research=Key Research Outputs, projects, people, news(메뉴 밖), pi=PI 개인 이력(메뉴 밖)), `_data/members.yml`, `_data/projects.yml`, `_bibliography/papers.bib`, `_news/`
- 설정: `_config.yml` (url/baseurl, 기능 플래그, 폰트 URL, scholar 저자 강조)
- 로컬 오버라이드(gem 파일을 같은 경로로 덮음): `_sass/_variables.scss`, `_sass/_themes.scss`, `_sass/_typography.scss`, `_includes/footer.liquid`, `_includes/header.liquid`(내비게이션 왼쪽 픽셀 마크)
  - 다른 gem 파일을 덮어야 하면 같은 경로에 파일을 두면 된다(`_layouts/`, `_includes/`). 원본은 https://github.com/al-org-dev/al-folio-core
- 배포: `.github/workflows/deploy.yml` 하나만 남김. `main` 푸시 → `gh-pages` 브랜치로 배포.

## 규칙

- 팔레트: 흰 배경 / 검정(#111111) 본문 / 파랑(#004de5) 하나. 보조 텍스트만 회색. 다크 모드 끔(`enable_darkmode: false`). 새 색을 추가하지 말 것.
- **영문 전용.** 사이트 본문·데이터·bib에 한국어를 넣지 않는다(교수님 지시, 2026-08-30).
- 랩 실적과 PI 개인 이력을 섞지 않는다: 랩 결성 이후 활동은 `_data/projects.yml`·`_news/`, PI의 이전 작업은 `_pages/pi.md`.
- 진행 중인 건(넥센·서울대 협업 등)은 한 문장 수준으로만 쓰고 예산·상대 이름·저널명을 적지 않는다. 과장 금지. **넥센은 내용 비공개**: 교수님이 준 한 문장("NEXEN, Future Concept Mobility Collaboration, next-generation mobility systems encompassing autonomous robotics, user-inclusive vehicles, and a cross-domain mobility ecosystem") 외에 산출물·주관 부서·일정·예산을 적지 않는다.
- research 페이지는 `papers.bib` 하나로 생성한다: 진행 중 항목(@misc, `abbr = {Ongoing}`/`{Submitted}`)과 논문을 섞어 `year` 내림차순 + `sortkey` 오름차순.
- 뉴스 날짜는 공지일 기준(Jekyll은 미래 날짜 글을 빌드에서 뺀다). 예정 항목은 본문을 "Upcoming:"으로 시작한다.
- `baseurl` 규칙: GitHub Pages 프로젝트 주소(`heeseonkimsun.github.io/agxlab.io`)일 때는 `/agxlab.io`, 커스텀 도메인 연결 후에는 빈 값. 링크는 항상 `relative_url` 필터를 거친다.
- 논문은 검증된 서지만 넣는다(DOI 확인). 추정 항목을 만들지 않는다.
- 이 PC에는 Ruby/Jekyll/Docker가 없다. 로컬 빌드 대신 푸시 후 Actions 결과와 배포 페이지 스크린샷으로 확인한다.

## 참고

- al-folio 문서: `docs/CUSTOMIZE.md`, `docs/INSTALL.md`, `AGENTS.md`(스타터 리포 규칙. "stop sign"의 경로 제한은 스타터 리포 자체에만 적용되고 사용자 사이트에는 적용되지 않는다)
