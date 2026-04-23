---
name: app-architect
description: |
  App Architect v1.1. 도메인→패턴매칭→설계→UX_CHECKLIST→와이어프레임HTML. 28도메인×190+앱 패턴DB. 일반/TURBO 2모드.
  P1: 앱설계, 앱기획, 앱아키텍트, 플랫폼설계, 서비스설계, 앱목업, 와이어프레임, 화면설계, 앱빌더, 서비스기획, 터보앱설계, TURBO.
  P2: 설계해줘, 목업만들어줘, design app, build mockup.
  P3: app architecture, wireframe, service blueprint, turbo design.
  P5: .html로, .md로, 와이어프레임으로.
  NOT: 단일화면UI(→ui-action-designer), 사업전략(→biz-skill), BP(→bp-guide), 재무(→financial-model), 디자인(→design-skill).
"@uses":
  - references/tokens.md
  - references/snippets.md
  - references/forbidden.md
  - references/qc.md
  - references/domain-patterns.md
  - references/beyond-patterns.md
  - references/ux-principles.md
---
# App Architect

앱설계·앱기획·앱아키텍트·플랫폼설계·서비스설계·앱목업·화면설계·앱빌더·서비스기획·터보앱설계 — 도메인 패턴 매칭 기반 와이어프레임 빌더.

사업방향 입력 → 도메인 패턴 매칭 → 기존을 초월하는 서비스 설계 → 와이어프레임 HTML 산출.

---

## 4블록 참조 구조

html-skill-refactor spine 공통. 허브형 스킬이라 **4블록=인덱스**, 풀스펙은 기존 3 스포크에 유지.

| 블록 | 역할 | 로드 시점 |
|------|------|-----------|
| `references/tokens.md` | 4축·진보 매트릭스·UX_CHECKLIST 5·HTML 토큰·도메인 라우팅 | ②·③ 진입시 |
| `references/snippets.md` | 단계별 스포크 매핑·입력 3분기·HTML 스니펫·한글 더미 | ①~④ 전단계 |
| `references/forbidden.md` | 절대 규칙 6·UX FAIL·더미·HTML·도메인·TURBO·로딩 금지 | 전단계 |
| `references/qc.md` | 절대 규칙 6·UX 5원리·HTML·블루프린트·매트릭스·TURBO·설치 QC | ③-b·④ |

**로딩 규칙:** 4블록은 **인덱스**. 실제 상세는 기존 3 스포크(domain-patterns·beyond-patterns·ux-principles)로 위임.

---

## ⛔ 절대 규칙

| # | 규칙 | 이유 |
|---|------|------|
| 1 | **패턴 DB 먼저** — 설계 전 반드시 `→ references/domain-patterns.md` 로딩 후 해당 도메인 패턴 확인 | 기억 재구성 = 패턴 누락. DB가 190+앱 축적된 근거 |
| 2 | **초월 설계** — 기존 패턴을 그대로 복사 ✗. 반드시 `→ references/beyond-patterns.md`의 진보원칙 1개+ 적용 | 패턴 복사는 미투. 차별화 없으면 스킬 가치 없음 |
| 3 | **4축 정합성** — 도메인-비즈목표-비즈모델-UX 4축이 서로 모순 없이 정렬 | 예쁜 UX인데 수익모델과 충돌하면 실패 |
| 4 | **HTML 산출 필수** — 설계 결과는 클릭 가능한 와이어프레임 HTML로 반드시 산출 | 문서만으로는 형이 판단 불가. 눈으로 봐야 함 |
| 5 | **핑퐁 금지** — Phase 1에서 1회 질문 후 바로 설계 진행. 추가 질문 없이 가정 후 진행 | 빠른 목업이 목적. 완벽한 요구사항 수집이 아님 |
| 6 | **UX_CHECKLIST 필수** — ④ HTML 산출 직전 `@ref: references/ux-principles.md#A-N2,N4,N6` + `#B-D1,D3` 검증. 미수행=FAIL | 와이어프레임이 사용자 언어 괴리·일관성 붕괴·어포던스 없음으로 전락 방지 |

---

## 실행 흐름

```
① 입력 파악 + 도메인 매칭 → ② 패턴 분석 + 진보 설계 → ③ 서비스 블루프린트 → ③-b UX_CHECKLIST → ④ 와이어프레임 HTML 산출
```

**UX 원리 허브:** `@ref: references/ux-principles.md` — 이 스킬은 N2·N4·N6 + D1·D3 코어 5개 적용. 필요시 §F 30초 체크리스트 사용.

### ① 입력 파악 + 도메인 매칭

```
입력 유형:
A. "~같은 앱 만들고 싶어" → 레퍼런스 앱 존재. DB에서 직접 매칭
B. "~분야 플랫폼" → 도메인 키워드로 매칭. 28도메인 중 1-2개 선택
C. "~문제를 해결하는 앱" → 문제→도메인 추론. 가장 가까운 도메인 매칭

질문 (1회, 최대 3개):
- 타겟 사용자는? (B2C/B2B/C2C)
- 핵심 해결 문제 1줄?
- 수익화 방향 (있으면)?

→ 답변 받으면 바로 ② 진행. 모르면 가정 명시 후 진행.
```

### ② 패턴 분석 + 진보 설계

```
1. `→ references/domain-patterns.md` 로드 — 매칭된 도메인 섹션만 읽기
2. 해당 도메인의 성공 앱 패턴 추출:
   - 공통 비즈모델 패턴
   - 공통 UX 패턴 (온보딩, 코어루프, 리텐션)
   - 크로스도메인 패턴 중 적용 가능한 것
3. `→ references/beyond-patterns.md` 로드 — 진보 원칙 선택
4. 진보 설계 매트릭스 작성:

| 설계 요소 | 기존 패턴 | 진보 적용 | 적용 원칙 |
|-----------|----------|----------|----------|
| 온보딩 | {기존} | {개선안} | {원칙명} |
| 코어루프 | {기존} | {개선안} | {원칙명} |
| 수익화 | {기존} | {개선안} | {원칙명} |
| 리텐션 | {기존} | {개선안} | {원칙명} |
```

### ③ 서비스 블루프린트

```
산출물 — md 파일:
1. 서비스 개요 (1문단)
2. 4축 정의
   - 도메인: {매칭 결과}
   - 비즈 목표: {성장 지표 2-3개}
   - 비즈 모델: {수익 구조}
   - 핵심 UX 패턴: {3-5개}
3. 화면 목록 + 흐름도 (텍스트)
   - 온보딩 → 홈 → 코어기능 → 결제/전환 → 리텐션루프
4. 화면별 핵심 기능 명세
5. 진보 설계 포인트 (기존 대비 차별화 3개+)
```

### ③-b UX_CHECKLIST — 와이어프레임 산출 직전 게이트

**역할:** 블루프린트→HTML 변환 직전 코어 5원리 검증. 허브 로드: `@ref: references/ux-principles.md#A-N2,N4,N6` + `#B-D1,D3`.

| 축 | 원리 | 체크 질문 | FAIL 시 |
|----|------|----------|--------|
| 언어 | N2 MATCH_REAL | 더미데이터·버튼명이 도메인 용어인가 (Lorem·Tab1 ✗) | ③로 롤백 — 도메인 어휘 재수집 |
| 일관 | N4 CONSISTENCY | 5화면 전반 네비·버튼 패턴 통일인가 | ② 진보설계 일관 원칙 재확인 |
| 기억 | N6 RECOGNITION | 탭 라벨·아이콘으로 기능 재인 가능한가 (외우게 하지 않음) | 탭 네비 라벨 재작성 |
| 시사 | D1 AFFORDANCE | 버튼은 눌러보이고 링크는 밑줄 등 행동 시사 | 컴포넌트 스타일 보강 |
| 응답 | D3 FEEDBACK | 탭 전환·클릭시 상태변화 가시화되는가 | JS 피드백 로직 추가 |

**🚪 게이트:** 5개 모두 PASS → ④ HTML 산출. 1개+ FAIL → 해당 단계 롤백 후 재검증 (1회 한). 상세 → 허브 §F.

### ④ 와이어프레임 HTML 산출

```
산출 규칙:
- 모바일 퍼스트 (max-width: 430px, 센터 정렬)
- 탭 네비게이션 (하단 3-5개)
- 각 탭 = 주요 화면 1개
- 클릭하면 탭 전환 (JS)
- 컬러: 그레이스케일 베이스 + 브랜드 컬러 1개 (사용자 미지정시 #2563EB)
- 폰트: system-ui
- 실제 더미 데이터 (Lorem 금지, 도메인에 맞는 한글 데이터)
- 단일 HTML 파일 (CSS+JS 인라인)

필수 화면:
1. 온보딩/로그인
2. 홈/피드/검색 (코어)
3. 상세 (아이템/프로필/콘텐츠)
4. 행동 (구매/예약/메시지/생성)
5. 마이페이지/설정

저장: /sessions/{session-id}/mnt/outputs/{앱이름}-wireframe.html
```

---

## 도메인 패턴

**도메인 패턴 외부화:** 도메인×패턴 매핑 데이터는 `references/domain-patterns.md`에 단일 관리. 본체에는 라우팅 로직만 유지.

## 도메인 자동 매칭 테이블

28도메인 키워드→도메인 라우팅 → `references/tokens.md §6`

---

## TURBO 모드

**트리거:** "터보로 설계" · "TURBO" · "앱 아키텍트 터보" 명시.

**불변 (시퀀셜):** ① 도메인 매칭·② 패턴DB/진보 원칙 로딩·③-b UX_CHECKLIST·④ HTML 최종 통합·Lorem/John Doe 차단 검증.

**병렬 타겟:** ② 매트릭스 4행(온보딩·코어루프·수익화·리텐션)·③ 5화면 기능 명세·④ 5화면 HTML 블록.

**품질 방어:** 화면 간 토큰·용어 불일치·N2/N4 위반·진보 원칙 중복·Lorem 혼입 → 재드래프트·시퀀셜 복귀. 상세 → `forbidden.md §6`·`qc.md §6`.

**예상 단축:** 45~60%.


## Gotchas

| 함정 | 대응 |
|------|------|
| 도메인 2+ 걸침 | 1차 확정 후 2차 크로스 적용 |
| 기존 앱 클론 요청 | 진보 원칙 2+ 필수 |
| references 미로딩 | ② 전 로딩 확인 = FAIL |
| 한글 더미 누락 (Lorem·John Doe) | 도메인 실어휘 강제 |
| UX_CHECKLIST 스킵 후 HTML | ③-b 게이트 미통과 = FAIL |

**세부 금지·대응:** → `references/forbidden.md`


---

## Version

- v1.1 (2026-04-23) — html-skill-refactor spine 적용. 4블록 인덱스(tokens·snippets·forbidden·qc) 추가, 기존 3 스포크 유지(허브 특성상 풀스펙 분산). `## 4블록 참조 구조` 섹션 신설
- v1.0 — 초기
