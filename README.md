# AGX Lab website (agxlab.io)

Affective Game Experience Lab, Chung-Ang University. Built with [al-folio](https://github.com/alshedivat/al-folio) (Jekyll), deployed by GitHub Actions to GitHub Pages.

## 자주 하는 편집

| 하고 싶은 일 | 고칠 파일 |
|---|---|
| 논문·진행 중 연구 추가 | `_bibliography/papers.bib` 에 BibTeX 항목 추가(research 페이지 "Key Research Outputs"에 최신순으로 표시). 같은 해 안의 순서는 `sortkey` (1, 2, 3…) 로, 진행 중 항목은 `abbr = {Ongoing}` 처럼 상태를 적음. 홈에 노출하려면 `selected = {true}` |
| 구성원 추가·수정 | `_data/members.yml` 한 블록 + 사진을 `assets/img/members/` 에 정사각형(약 480px) JPG로. 사진이 없으면 `image` 줄을 빼면 이니셜로 표시 |
| 소식 추가 | `_news/YYYY-MM-DD-slug.md` (짧은 한 줄이면 `inline: true`). 날짜는 공지일 기준, 예정 항목은 본문을 "Upcoming:"으로 시작 |
| 프로젝트·협업 추가 | `_data/projects.yml` 한 블록(`start` 날짜로 최신순 정렬, `status`는 ongoing/upcoming/completed, 숨기려면 `draft: true`) |
| 구성원 연구 분야 | `_data/members.yml` 의 `research:` 한 줄 (확인 전에는 비워 둠) |
| 홈 문안·연구 영역·모집 안내 | `_pages/about.md` |
| 연구 페이지 | `_pages/research.md` (목록 자체는 papers.bib에서 생성). 논문 썸네일은 `assets/img/publication_preview/` |
| 색·글꼴 | `_sass/_variables.scss` (색 값), `_sass/_themes.scss` (역할별 색), `_sass/_typography.scss` (글꼴·구성원 그리드) |
| 사이트 제목·설명·메뉴 기능 | `_config.yml` |

파일을 고쳐 `main` 브랜치에 커밋·푸시하면 GitHub Actions가 빌드해 `gh-pages` 브랜치로 배포합니다(2~4분). 진행 상황은 리포의 **Actions** 탭.

## 도메인 연결 (agxlab.io)

1. 리포 루트에 `CNAME` 파일을 만들고 내용에 `agxlab.io` 한 줄.
2. `_config.yml` 에서 `url: https://agxlab.io`, `baseurl:` (빈 값) 으로 변경.
3. 도메인 DNS: `A` 레코드 4개(185.199.108.153 / 109.153 / 110.153 / 111.153) + `www` `CNAME` → `heeseonkimsun.github.io`.
4. 리포 Settings → Pages → Custom domain 에 `agxlab.io` 입력, Enforce HTTPS 체크.

## 로컬 미리보기(선택)

Ruby + Bundler 가 있으면 `bundle install && bundle exec jekyll serve` 후 `http://localhost:4000/agxlab.io/`.
Docker 가 있으면 `docker compose up`. 둘 다 없으면 푸시 후 GitHub Pages 결과로 확인해도 됩니다.

## 디자인 규칙

흰 배경(#ffffff), 본문 검정(#111111), 강조색은 파랑 하나(#004de5). 보조 텍스트(날짜·소속)만 회색(#6b6b6b). 다크 모드 없음. 사이트 본문은 영문 전용.
