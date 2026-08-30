# AGX Lab website (agxlab.io)

Affective Game Experience Lab, Chung-Ang University. Built with [al-folio](https://github.com/alshedivat/al-folio) (Jekyll), deployed by GitHub Actions to GitHub Pages.

## 자주 하는 편집

| 하고 싶은 일 | 고칠 파일 |
|---|---|
| 논문 추가 | `_bibliography/papers.bib` 에 BibTeX 항목 추가. 홈에 노출하려면 `selected = {true}` |
| 구성원 추가·수정 | `_data/members.yml` 한 블록 + 사진을 `assets/img/members/` 에 정사각형(약 480px) JPG로 |
| 소식 추가 | `_news/YYYY-MM-DD-slug.md` (짧은 한 줄이면 `inline: true`) |
| 홈 문안·연구 영역·모집 안내 | `_pages/about.md` |
| 연구 페이지(최근 연구 이미지, 주요 성과 목록) | `_pages/research.md`, 이미지는 `assets/img/research/` |
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

흰 배경(#ffffff), 본문 검정(#111111), 강조색은 파랑 하나(#004de5). 보조 텍스트(날짜·소속)만 회색(#6b6b6b). 다크 모드 없음.
