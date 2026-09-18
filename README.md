# VOIDBOX WebAR 프로토타입 — 조경수목 정보 패널

## 구성
- `index.html` : 단일 파일 (A-Frame 1.5 + MindAR 1.2.5, CDN 로딩)
- `assets/card.mind` : **임시 마커** (MindAR 공식 샘플). 회사 로고로 만든 .mind로 교체
- `assets/card.png` : 임시 마커 인쇄용 이미지 (테스트 시 화면에 띄우거나 출력)

## 배포 (HTTPS 필수 — 카메라 권한)
GitHub Pages: 리포 루트에 그대로 업로드 → Settings > Pages > main / root  
Vercel: 폴더 드래그 앤 드롭 (빌드 설정 없음)

## 마커 교체
1. https://hiukim.github.io/mind-ar-js-doc/tools/compile 에서 로고 이미지 업로드 → `targets.mind` 다운로드
2. `assets/card.mind` 를 덮어쓰기 (또는 `index.html` 의 `const MARKER` 경로 수정)
3. 로고는 대비가 높고 디테일이 많을수록 인식이 안정적. 단색·심플 로고면 명함 전체(로고+텍스트)를 마커로 컴파일 권장

## 데스크톱 프리뷰 (카메라 없이 패널 확인)
`index.html?preview=1`

## 데이터 수정
`index.html` 상단 `const TREE = {...}` 만 바꾸면 패널 3종(기본정보/생육데이터/관리이력)에 반영

## 시연 팁
- iOS Safari / Android Chrome 모두 동작. 카톡 인앱 브라우저는 카메라가 막힐 수 있어 QR → 기본 브라우저로 열기 권장
- 명함은 평평하게, 조명 반사 없이. 카메라와 20~40cm 거리
- 인식 후 하단 탭 버튼으로 패널 전환
