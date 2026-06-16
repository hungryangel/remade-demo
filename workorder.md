# REMADE 사이트 — 코덱스 작업 워크오더

## 개요
REMADE(리메이드) 반영구 브랜드 사이트. 정적/SSG, 모바일 우선.
`index.html`은 지금까지 만든 빌드이자 출발점이다. 데이터·자산·배포를 채우고, **디자인도 자유롭게 다듬어** 완성도를 끌어올린다.

## 현재 디자인 방향 (출발점 — 발전시켜도 됨)
- 올블랙 캔버스(#070A07) + 초록 정체성. 토큰: `--green #2BA350`, `--green-bright #62DC8C`, 본문 텍스트 `#ECF1EA`, 디스플레이/제목은 초록.
- 서체: 디스플레이 Cormorant Garamond, 한글 Noto Serif KR, 본문 Pretendard.
- 인트로: 초록 글로우 라이트박스(가운데 검은 'REMADE' 세리프) → 스크롤 시 초록 페이드아웃 → 영어 문구 등장(1줄 "We don't draw eyebrows." 페이드업 먼저, 2줄 "We rebuild the impression you leave." 좌→우 와이프). 첫 화면 내비 숨김.
- 타이포그래피 서울식 에디토리얼: 세리프 디스플레이, 영문/한글 이중 라벨, 헤어라인 구조, 넉넉한 여백, 풋터 초대형 워드마크.

> 이 방향은 고정값이 아니라 **기준선**이다. 더 나은 안이 있으면 타이포·간격·모션·섹션 구성·컬러 밸런스 등 자유롭게 개선·재구성해도 된다. 브랜드의 블랙+초록 정체성과 매장 라이트박스 무드만 이어지면 된다.

## 할 일

### 1. 구조 · 정리
- `index.html` + `/assets`. 캠페인 이미지는 `./assets/campaign.jpg`로 연결돼 있음.
- 미사용 CSS 정돈(.aa-toggle, .foot-top, .pin, .lightwall 등 잔재).

### 2. 지점 데이터 (실데이터)
아래 네이버 플레이스 9곳을 열어 **지점명·주소·좌표** 수집 → 단일 `branches[]` 배열로 목록과 지도 핀을 같은 데이터에서 렌더. 한국 지도는 정확한 GIS(geojson/svg)로 교체하고 좌표로 핀 배치.
- https://naver.me/xnO57cVJ
- https://naver.me/xAAYLlsO
- https://naver.me/x6xvkdyU
- https://naver.me/517wntyh
- https://naver.me/GScMO6cr
- https://naver.me/GOPKK35H
- https://naver.me/56XeK9SJ
- https://naver.me/G2YhJhl5
- https://naver.me/FkaApCRt

### 3. 자산 교체
- 포트폴리오 전후 사진(동의받은 실물).
- 후기·숫자 실데이터(가짜 placeholder 제거).
- 인스타/스레드/유튜브, 사업자정보·연락처.
- 실제 REMADE 서체가 있으면 적용.

### 4. 전환 동선
- 예약 / 창업·교육 CTA를 실제 퍼널로(네이버 예약 / 구글폼 / 카카오 채널 등).

### 5. SEO / AEO
- JSON-LD(LocalBusiness + 지점 9개), meta·OG, sitemap.xml, robots.txt.

### 6. 모바일 QA (첫 접점이 모바일)
- svh·sticky 동작, 인트로 스크롤 길이, 히어로/영어 문구가 한 화면에 들어오는지.

### 7. 배포
- GitHub → Vercel(또는 Cloudflare Pages) 자동배포 + 도메인 연결.

## 산출물
- 배포 URL, 레포 주소, 변경 요약.
