# snippets.md — App Architect 스니펫 인덱스

html-skill-refactor spine 4블록 중 **snippets**. 단계별·진보 원칙·HTML 구조 인덱스.

## §1. 단계별 스포크 매핑

| 단계 | 로드 파일 | 스니펫 종류 |
|------|----------|------------|
| ① 입력 + 도메인 매칭 | SKILL.md §도메인 매칭 | 키워드→도메인 |
| ② 패턴 분석 | `domain-patterns.md` | 도메인별 성공앱 패턴 |
| ② 진보 설계 | `beyond-patterns.md` | 진보 원칙 카탈로그 |
| ③ 블루프린트 | — | md 4축 + 화면 목록·기능 명세 |
| ③-b UX_CHECKLIST | `ux-principles.md#A-N2,N4,N6` + `#B-D1,D3` | 5원리 체크 |
| ④ HTML 산출 | SKILL.md §④ 산출 규칙 | 단일 HTML 템플릿 |

## §2. 입력 유형 3분기 (§①)

```
A. "~같은 앱" → 레퍼런스 앱 직접 매칭 (DB 조회)
B. "~분야 플랫폼" → 도메인 키워드 매칭 (28도메인 중 1~2)
C. "~문제 해결" → 문제→도메인 추론 (가장 근접 매칭)
```

**1회 최대 3질문:** 타겟(B2C/B2B/C2C)·핵심 문제 1줄·수익화 방향. 답변 받으면 바로 ② 진행.

## §3. HTML 구조 스니펫 (§④)

```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>{앱이름}</title>
  <style>
    :root { --brand: #2563EB; --bg: #fff; --text: #1a1a1a; --gray: #f5f5f5; }
    body { max-width: 430px; margin: 0 auto; font-family: system-ui; }
    .screen { display: none; }
    .screen.active { display: block; }
    .tabbar { position: fixed; bottom: 0; width: 100%; max-width: 430px; display: flex; }
    .tab { flex: 1; padding: 12px; text-align: center; }
    .tab.active { color: var(--brand); }
  </style>
</head>
<body>
  <main>
    <section class="screen active" id="onboarding">...</section>
    <section class="screen" id="home">...</section>
    <section class="screen" id="detail">...</section>
    <section class="screen" id="action">...</section>
    <section class="screen" id="my">...</section>
  </main>
  <nav class="tabbar">...</nav>
  <script>
    // 탭 전환
    document.querySelectorAll('.tab').forEach(t => t.onclick = () => {...});
  </script>
</body>
</html>
```

## §4. 더미 데이터 원칙 (§④)

- **한글 실어휘 필수:** Lorem·John Doe·"상품1"·"카테고리A" = N2 FAIL
- **도메인 맞춤:**
  - 음식배달 → "매콤 닭갈비 세트 18,900원"
  - 숙박 → "제주 협재 오션뷰 빌라 1박 245,000원"
  - 소셜 → "@minji_travel · 제주 2박 3일 기록"
- **숫자 단위:** 원(₩)·km·명 등 한국 맥락

## §5. 공통 프리미티브

### 크로스도메인 패턴 (도메인 2개+ 걸침)
- 1차 도메인 선정 → 2차 도메인 패턴 크로스 적용
- 완전 신규 분야 → 유사 도메인 2개 교차 + 크로스도메인 패턴 15개 중 선택

### 로딩 원칙
- `domain-patterns.md` = ② 1회 (매칭 도메인 섹션만)
- `beyond-patterns.md` = ② 1회 (진보 원칙만)
- `ux-principles.md` = ③-b 1회 (N2·N4·N6 + D1·D3만)
