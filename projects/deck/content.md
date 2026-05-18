# Deck v4 · 텍스트 콘텐츠 (index.html 적용 완료)

index.html에 모두 반영되어 있습니다 (`http://localhost:8765/projects/deck-v4/`). 이 마크다운은 텍스트 단위 교열 참고용. 수정 사항 알려주시면 일괄 반영합니다.

---

## 변경 요약

| 항목 | 변경 내용 |
|---|---|
| #1 Cover | "신인식 + Project Portfolio" 임팩트 표지로 재작성 (3 프로젝트 카드 제거) |
| #2 Project Index | 비교 카드 제거 → 단순 프로젝트 목차로 |
| 표지 슬라이드 (NEW) | 각 프로젝트 표지 3장 추가 (Lumiere · Leaderboard · Scrim Manager) |
| #11 Leaderboard Capture | 제거 |
| #16 Leaderboard Cost/Ops | 제거 |
| #20 Bot Flow | "관리자 조회" → "유저 푸시 알림"으로 재작성 (#21 Notifications) |
| #22 Vision OCR/POTM | POTM 슬라이드 신설 (#23) · main 이미지 POTM 패널 크롭 |
| #23 Data Model | 제거 |
| BT Ranking 슬라이드 | 완전 제거 (POTM 슬라이드로 알고리즘 콘텐츠 흡수) |
| Scrim Manager 표현 | "내전 운영" → "외부 팀과의 스크림 경기와 내전 경기" 일관 표기 |

**최종 슬라이드 수: 26장** (제거 -4: #11 Capture · #16 Cost/Ops · #23 Data Model · BT Ranking / 추가 +4: 표지 3 + 목차 형태 유지)

---

## 새 deck 구조 (26장)

```
 #1  Cover
 #2  Project Index (목차, 단순화)
 #3  Lumiere 표지 (NEW)
 #4  Lumiere · Problem
 #5  Lumiere · Product
 #6  Lumiere · Architecture
 #7  Lumiere · Template
 #8  Lumiere · Scale
 #9  Lumiere · Tradeoff
 #10 Lumiere · Takeaway
 #11 Overwatch Leaderboard Crawler 표지 (NEW)
 #12 Overwatch Leaderboard Crawler · Problem
 #13 Overwatch Leaderboard Crawler · CV Pipeline
 #14 Overwatch Leaderboard Crawler · Data Path
 #15 Overwatch Leaderboard Crawler · Public Surface
 #16 Overwatch Leaderboard Crawler · Reliability
 #17 Overwatch Leaderboard Crawler · Takeaway
 #18 Scrim Manager 표지 (NEW)
 #19 Scrim Manager · Problem
 #20 Scrim Manager · Web App
 #21 Scrim Manager · Notifications (구 Bot Flow 재작성)
 #22 Scrim Manager · Vision OCR
 #23 Scrim Manager · POTM (구 Ranking 위치, POTM 패널 surface 중심)
 #24 Scrim Manager · Adoption
 #25 Scrim Manager · Operations
 #26 Closing
```

### 메모: Bradley-Terry Ranking 슬라이드 처리
- ✅ 결정: BT Ranking 슬라이드 완전 제거. POTM 슬라이드 (#23)의 알고리즘 노트로 핵심 메시지 흡수.
- 복구 원하면 알려주세요 (별도 슬라이드 신설 → 27장으로 늘림).

---

# 슬라이드별 텍스트 콘텐츠

---

## #1 Cover

임팩트 표지 — 큰 한글 이름 + 영문 타이틀 강조 (3 프로젝트 카드 제거).

**META**: DECK · 1 / 26 | portfolio cover
**EYEBROW**: SHIN INSIK
**NAME (h1, 한글 큰 타이포 9em / weight 800)**: 신인식
**TITLE (h2, 영문 큰 타이포 3.6em / weight 300)**: Project Portfolio
**ACCENT**: 3색 액센트 막대 (Lumiere blue · Leaderboard orange · Scrim red)

---

## #2 Project Index (목차)

**TITLE**: Project Index

**목차 항목**:

1. **Lumiere** · 대입 정시 성적 및 합격 가능성 분석 보고서 · 2017-2020 · pp.3-10
2. **Leaderboard Pipeline** · 영웅 성능 데이터 수집·분석 · 2023-2026 · pp.11-17
3. **Scrim Manager** · 외부 팀과의 스크림 경기와 내전 경기 운영 도구 · 2025 · 현재 · pp.18-25

---

## #3 Lumiere 표지 (NEW)

**PROJECT**: Lumiere
**PERIOD**: 2017-2020
**TAGLINE**: 수능 점수를 입력하면 성적 및 합격 가능성 분석 보고서를 받아볼 수 있는 서비스

**NEXT_UP**:
- Problem · 정시 지원 의사결정의 비용과 정보 격차
- Product · 수능 점수에서 PDF 보고서까지
- Architecture · 확장 가능성과 휴면 비용 0원을 위한 설계
- Scale · 10만+ 학생 · 150,000+ PDF
- Report · 모집단위별 합격 가능성을 직관적인 시각화로 표현

---

## #4 Lumiere · Problem · Before/After

**TITLE**: 정시 정보에 대한 접근성을 높여 정보 격차를 해소했습니다.
**SUB**: 누구나 수능 점수로 합격 가능성을 판단할 수 있습니다. 컨설팅 비용, 대기 시간, 지역별 정보 격차를 줄이는 쪽에 기획 의도를 두었습니다.

**SVG bullets (BEFORE/AFTER 박스 안)** — 6개 항목 모두 dash prefix 없이 명사구로:
- BEFORE: 회당 수십만원 비용 / 대기 순번의 기다림 / 지역에 따른 정보 격차
- AFTER: 무료 공개 · 진입장벽 없음 / 즉시 반복 시뮬레이션 / 3개년 누적 10만+ 학생
비고: `환산점수 → 등수 → 합격가능성`은 `고속성장 수능 점수 계산기 데이터에 누구나 쉽게 접근`으로 교체

---

## #5 Lumiere · Product · Product Surface

**TITLE**: 수능 점수만으로 PDF 보고서를 생성합니다.
**SUB**: 표준점수, 백분위, 등급과 학교별 환산공식을 결합했습니다. 학생은 첫 화면에서 전국 위치와 지원 가능성을 함께 확인합니다.

**notes** (3개):
- **surface · 1** — 성적 요약: 표준점수, 백분위, 등급, 상위누적을 한 행에 묶어 정량 판단 기준을 제공합니다.
- **surface · 2** — 전국 위치: 표준점수 합과 백분위 합을 기준으로 전국 석차와 상위누적백분위를 계산합니다.
- **surface · 3** — 응시자 기준: 수학 가/나형 응시자 표본을 기준으로, 학생이 자신의 계열에서 위치를 정확하게 가늠하게 했습니다.

---

## #6 Lumiere · Architecture · System Diagram

**TITLE**: 단일 Lambda에서 보고서 생성까지 처리합니다.
**SUB**: Zappa로 패키징한 Flask 앱이 학교별 환산 모듈과 wkhtmltopdf를 호출합니다. 요청 폭증과 휴면 기간 비용을 모두 고려한 serverless 구조입니다.

---

## #7 Lumiere · Scale · Metric Proof

**TITLE**: 단일 Lambda로 10만+ 학생을 처리했습니다.
**SUB**: 2017년부터 2020년까지 3개년 동안 운영했습니다. 정시 모집 기간 동안 피크가 반복되는 워크로드에서 유저 100,000+명과 PDF 150,000+건을 처리했습니다.

---

## #8 Lumiere · Takeaway · Product Surface

**TITLE**: 모집단위별 합격 가능성을 직관적으로 표현했습니다.
**SUB**: 표준점수, 환산점수, 모집단위 위치, 4단계 가능성을 한 보고서에 묶었습니다.

**notes** (3개):
- **layer · 1** — 모집단위 기준: 학교 단위가 아니라 모집단위, 모집군, 정원 단위로 추정합니다. 가군, 나군, 다군을 분리해 처리했습니다.
- **layer · 2** — 점수와 상위누적백분위: 환산점수와 상위누적백분위를 함께 표기합니다. 한 지표만으로 판단하기 어려운 경계 케이스를 줄였습니다.
- **layer · 3** — 4단계 색상: 최초합, 추가합, 불합격, 경계를 한 줄 막대로 표시합니다. 긴 표를 읽지 않아도 결정을 내릴 수 있게 했습니다.

---

## #9 Leaderboard 표지 (NEW)

**PROJECT**: Overwatch Leaderboard Crawler
**PERIOD**: 2023-2026
**TAGLINE**: 공식 API가 없는 영웅 성능 데이터를 매일 수집하는 27개월 무중단 파이프라인.

**NEXT_UP (6개)**:
- Problem · 메타 분석을 위해 데이터가 필요
- CV Pipeline · 클라이언트 조작 자동화 및 컴퓨터 비전 기반 분석
- Architecture · 캡처·변환·보관을 AWS에서 자동화
- Visualization · owtics.gg에서 시계열 형태로 제공
- Reliability · 27개월 동안의 데이터 누적
- Takeaway · 공식 API 없이 27개월 매일 갱신

---

## #11 Leaderboard · Problem · Product Surface

**TITLE**: 공식 API가 없는 메타 데이터를 매일 수집합니다.
**SUB**: Blizzard는 2025년까지 영웅 통계 API를 제공하지 않았습니다. 유일한 데이터인 상위 500위 리더보드를 데이터 원천으로 삼았습니다.

**notes** (3개):
- **source · 데이터 원천** — API 없음: 공식 API가 없어서 화면 캡처가 유일한 방법이었습니다. 클라이언트 조작을 자동화하여 리더보드에 접근했습니다.
- **scope · 일일 분량** — 3개 지역, 3개 역할을 매일 같은 시각에 수집합니다. 하루 약 1,350장의 PNG 이미지와 약 4,500명 유저의 데이터가 수집됩니다.
- **payload · 다섯 개의 필드* — Rank, tier, name, count, heroes를 인식합니다. 각 필드마다 적합한 방법론이 달랐습니다.

---

## #12 Leaderboard · CV Pipeline · Pipeline Frame

**TITLE**: 한 행을 다섯 가지 기법으로 분해합니다.
**SUB**: 리더보드의 한 행을 5개 필드로 나누고, 각 필드에 맞는 인식 방식을 적용했습니다.

**5-stage strip** (.stage12 그리드 유지):
- ① rank · 순위 · template match · "1"
- ② tier · 티어 · 등급 · HSV hue + template · "CHAMPION 5"
- ③ name · 플레이어 · 별명 · EasyOCR · "HYDRON · 말썽꾼"
- ④ count · 경기 수 · EasyOCR · "106"
- ⑤ heroes · 모스트 3 · Perceptual Hashing · "[reaper, cassidy, sojourn]"

---

## #13 Leaderboard · Data Path · System Diagram

**TITLE**: 캡처, 변환, 보관을 AWS 안에서 자동화했습니다.
**SUB**: EC2는 화면 캡처에 집중하고, Lambda는 분석과 데이터 리포트를 처리하며, S3는 원본 이미지를 보관합니다.

---

## #14 Leaderboard · Public Surface · Product Surface

**TITLE**: 화면 캡처를 영웅 레이팅 시계열로 바꿉니다.
**SUB**: owtics.gg 개발팀과 협업하여 ICHI Rating을 제공했습니다. API contract를 정의하여 데이터를 리포트하고, 메타 변화를 시계열로 제공합니다.

**notes** (3개):
- **consumer · owtics.gg** — ICHI Rating: 탱, 딜, 힐 그룹별 영웅 레이팅 추이를 보여줍니다. 시즌 메타 변화를 한 줄 차트로 읽게 했습니다.
- **data report** — 캡처된 이미지에서 인식된 데이터를 API contract에 맞게 가공하여 공급했습니다.
- **contract · public** — 외부 의존 0: Blizzard 공식 API 없이도 owtics.gg가 매일 새로운 메타 데이터를 시각화할 수 있게 했습니다.

---

## #15 Leaderboard · Reliability · Metric Proof

**TITLE**: 27개월 동안의 영웅 메타 데이터를 쌓았습니다.
**SUB**: UI가 변경될 때마다 빠르게 대응했습니다. Template Matching, OCR, Perceptual Hash를 분리해 인식 기법을 모듈화한 선택이 유지보수 경량화의 핵심이었습니다.

---

## #16 Leaderboard · Takeaway · Metric Proof

**TITLE**: 공식 API 없이도 27개월간 매일 갱신했습니다.
**SUB**: 중요한 역량은 한 번 만든 스크립트가 아니라 지속적으로 운영하는 노하우입니다.
비고: 270이 아닌 1,350 PNG/일

---

## #17 Scrim Manager 표지 (NEW)

**PROJECT**: Scrim Manager
**PERIOD**: 2025 - · 현재
**TAGLINE**: 외부 팀과의 스크림 경기와 내전 경기를 한 도구로 묶은 풀스택 운영 도구.

**NEXT_UP (7개)**:
- Problem · 디스코드 DM에 의존하던 스케줄 관리를 웹 서비스로.
- Web App · 기존 워크플로우를 존중하는 설계
- Notifications · 유저에게 가는 Discord DM 흐름
- Vision OCR · 스크린샷으로부터 경기 기록 자동 인식
- POTM · Player of the Match를 선정하여 동기 부여
- Adoption · 53 WAU · 71 MAU · 100명 회원
- Operations · 모놀리식 아키텍처로 개발 및 유지보수 용이

---

## #19 Scrim Manager · Problem · Before/After

**TITLE**: 수십 통의 디스코드 DM을 없앴습니다.
**SUB**: 가능한 일정을 수집하고, 경기 일정을 공유하는 워크플로우가 모두 디스코드 DM을 통해 이루어졌습니다. 웹 페이지로 운영진들의 수고를 줄였습니다.

**notes** (3개):
- **before · manual** — 극한의 DM 노동: 멤버별로 가능한 시간을 매번 DM으로 재촉해야 했습니다. 운영진이 실수할 여지도 있었습니다.
- **after · grid** — 가용성 그리드: 요일과 시간대별로 누가 가능한지 한 화면에 표시합니다. 색상과 아이콘으로 역할 정보까지 같이 보입니다.
- **player · apply** — 빠르고 편리한 스케줄 등록: DM으로 가능한 시간을 작성하는 대신, 드래그 몇 번이면 가능한 시간을 제출할 수 있습니다.

---

## #20 Scrim Manager · Web App · Product Surface

**TITLE**: 첫 화면에 핵심 상태를 모았습니다.
**SUB**: 주간 스케줄, 팀 라인업 진행률, 다가오는 외부·내전 경기, 빠른 작업을 한 화면에 배치했습니다.

**notes** (3개):
- **widget · 1** — 주간 상태: 이번 주와 다음 주의 휴가 및 스케줄 등록 상태를 한 줄로 확인합니다.
- **widget · 2** — 라인업 진행률: 팀별 가용성 입력 완료율을 표시합니다. 누가 아직 입력하지 않았는지 바로 확인합니다.
- **widget · 3·4** — 빠른 작업: 예정된 외부 스크림과 내전, 내 스케줄, 전체 스케줄, 스크림 기록으로 바로 이동합니다.

---

## #21 Scrim Manager · Notifications · Pipeline Frame (구 Bot Flow 재작성)

**TITLE**: 공지사항을 유저에게 Discord DM으로 푸시합니다.
**SUB**: 스케줄 등록 요청부터 경기 생성·수정·취소·참여 변경까지, 멤버에게 알림을 보냅니다. 더 이상 운영진이 각 유저에게 DM을 보낼 필요가 없습니다.

**notes** (3개):
- **request · push** — 스케줄 등록 요청: 매주 등록 안 한 멤버에게 자동 DM. 가능한 시간을 미리 받아 매칭에 활용합니다.
- **events · 8+ types** — 경기 이벤트 알림: 생성·수정·취소·삭제·참여자 추가·제외·확정·리마인드까지. 외부 스크림과 내전 모두 같은 흐름으로 전달합니다.
- **link · web** — 웹 딥링크: 모든 DM에 "웹에서 열기" 버튼이 붙습니다. Discord에서 1-click으로 사이트의 경기 상세 페이지로 이동합니다.

### 메모: 다이어그램 구성
- ✅ 적용: 옵션 (a) — 좌측 Discord DM mockup 카드 2장 (스케줄 등록 요청 + 새 경기 등록) + 우측 9-event 카탈로그.

### 알림 종류 카탈로그 (참고, latan-stats 코드 기준)
```
📅 스케줄 등록 요청     · 매주 미등록자에게
✅ 스케줄 등록 완료     · 제출 확인 DM
🎮 새 경기 등록         · 참여자에게
📝 경기 일정 수정       · 참여자에게
➕ 경기 참여 등록       · 추가된 멤버에게
➖ 경기 참여 취소       · 제외된 멤버에게
❌ 경기 취소           · 참여자에게
🗑️ 경기 삭제           · 참여자에게
🔔 리마인드 (D-1 등)   · 참여자에게
```

---

## #22 Scrim Manager · Vision OCR · Product Surface

**TITLE**: 스크린샷을 등록하면 경기 기록을 대신합니다.
**SUB**: 인게임 스코어보드를 Qwen3-VL으로 인식하여 구조화했습니다.

**notes** (3개):
- **input** — 스크린샷 업로드: 5v5 매치 종료 화면을 업로드합니다.
- **engine · bedrock** — Qwen3-VL 호출: 닉네임 및 통계를 읽습니다. 높은 성능으로 강인한 인식률을 보여줍니다.
- **output** — 데이터 구조화: 영웅, K/D/A, 대미지, 치유, 경감을 인식하여 구조화합니다. SQLite에 저장해 다음 단계의 POTM 선정과 통계 UI를 렌더링합니다.

### 메모: main 이미지
- ✅ 적용: `assets/scrim/latan-2-stats.png` 유지 (영웅 선택 그리드 + 게임1 스탯 테이블).

---

## #23 Scrim Manager · POTM · Product Surface (구 Ranking 위치)

**TITLE**: 매치마다 Player-of-the-Match를 자동 선정합니다.
**SUB**: OCR로 들어온 스탯을 역할별 가중합으로 변환하고, 참여율 필터를 적용한 뒤 1위 플레이어를 선정합니다.

**notes** (3개):
- **algorithm · weighted sum** — 역할별 가중치: 탱커(킬·데스·대미지·경감) / 딜러(대미지·킬·데스·어시스트) / 힐러(치유·데스·대미지·어시스트·킬). Min-max 정규화 후 가중합으로 POTM 점수를 계산합니다.
- **filter · participation** — 참여율 필터: 적은 수의 게임에만 참여하여 잘한 플레이어는 제외합니다.

### 메모: main 이미지 (준비 완료)
- ✅ `assets/scrim/potm-panel.png` (745×160) — 사용자가 직접 크롭 + 익명화 완료.
- 포함: Play of the Match 헤더 · 탱커 뱃지 · 닉네임(블러) · 메타 "5/5 게임 참여 · 1등/10명 · 스코어 0.70" · 6 스탯 카드 (K 22.6 / A 11.0 / D 5.4 / DMG 13,756 / HEAL 3,188 / MIT 7,743 per 10분).

### 메모: Bradley-Terry Ranking 처리
- ✅ 적용: 옵션 (a) — Ranking 슬라이드 완전 제거. 핵심 알고리즘 메시지는 POTM 슬라이드의 notes에 흡수.

---

## #24 Scrim Manager · Adoption · Metric Proof

**TITLE**: 100명 중 53명의 회원이 매주 사용합니다.
**SUB**: 디스코드 스크림 팀 회원은 100명, 그 중 매주 스크림에 참여하는 회원은 53명입니다.

---

## #25 Scrim Manager · Operations · System Diagram

**TITLE**: 단일 프로세스가 웹, 봇, OCR을 함께 운영합니다.
**SUB**: 서비스 분리보다 배포 단순성, 비용, 개발 공수, 장애 지점 축소가 중요했습니다.

---

## #26 Closing · Metric Proof

**TITLE**: 수집, 자동화, 지속적인 운영까지를 목표합니다.
**SUB**: 세 프로젝트는 서로 다른 도메인이지만 같은 역량을 증명합니다. 데이터를 구조화하고, 비용과 안정성을 고려해 연 단위로 운영할 수 있습니다.
**CAPTION**: SHIN INSIK · p0rygon.github.io · 2026.05 | contact: gms04246@gmail.com

**3 evidence 카드**:
- LUMIERE · SCALE: 100,000+ 학생 가입자 / 150,000+ PDF 보고서 출력 / 3개년 운영 · 2018 - 2021학년도 정시 모집
- LEADERBOARD · AUTOMATION: 27개월 운영 / 6.6M+ 누적 처리 행 / 0 외부 API · 2023.10 - 2026.01
- SCRIM · ADOPTION: 100+ 등록 플레이어 / 53 WAU·71 MAU / 매주 외부 스크림과 내전 운영 · 2025 - 현재

---

# 적용 상태 (모두 index.html 반영 완료)

1. ✅ Ranking 슬라이드: 완전 제거. 알고리즘은 #23 POTM 슬라이드의 notes에 흡수.
2. ✅ #21 Notifications 다이어그램: DM mockup 2개 + 9-event 카탈로그 (옵션 a)
3. ✅ POTM 패널 이미지: assets/scrim/potm-panel.png
4. ✅ Vision OCR (#22) main 이미지: latan-2-stats 유지
5. ✅ 표지 슬라이드 디자인 (Lumiere · Leaderboard · Scrim): 좌측 큰 타이포 + 우측 Coming up 리스트
6. ✅ #1 Cover: 신인식 + Project Portfolio 임팩트 표지

---

# 교열 후 알려줄 것

각 슬라이드별로 수정 사항을 알려주시면 index.html에 일괄 반영합니다. 마크다운을 직접 수정해서 보내주셔도 됩니다.
