# app-architect

> 🇺🇸 [English README](./README.md)

**도메인 입력→성공앱 패턴매칭→서비스설계→와이어프레임HTML 산출. 28도메인×190+앱 패턴DB 기반 플랫폼 목업 빌더.**

## 사전 요구

- **Claude Cowork 또는 Claude Code** 환경

## 목표

대부분의 앱 설계는 백지에서 시작하거나 경쟁사 1개를 복사한다. app-architect는 반대로 접근한다: 28개 산업 도메인(여행, 핀테크, 이커머스, AI/챗봇, 펫, 그로서리 등)의 검증된 패턴을 로딩하고, 기존 앱을 초월하는 12개 진보 설계 원칙을 적용해서 차별화된 서비스 설계와 작동하는 모바일 와이어프레임을 한번에 산출한다.

## 사용 시점 & 방법

새 앱이나 플랫폼을 구상할 때 발동. 만들고 싶은 걸 설명하면 된다 — 레퍼런스 앱("에어비앤비 같은 펫 서비스"), 도메인("펫 커뮤니티 플랫폼"), 또는 문제("동네 수의사 찾기 어려운 문제 해결"). 최대 3개 질문 후 4단계 파이프라인 자동 진행: 도메인 매칭 → 패턴 분석 + 진보 원칙 적용 → 서비스 블루프린트 → 와이어프레임 HTML 산출.

## 사용 사례

| 상황 | 프롬프트 | 동작 |
|---|---|---|
| 새 플랫폼 아이디어 | `"펫 커뮤니티 앱 설계해줘"` | 펫 도메인 매칭 → 6개 앱 패턴 로딩 → 진보 원칙 적용 → 블루프린트 + HTML 산출 |
| 레퍼런스 기반 | `"에어비앤비 같은 숙박 앱"` | 숙박 도메인 매칭 → Airbnb 패턴 분석 → 개선된 버전 설계 |
| 문제 기반 | `"동네 빈집 문제 해결하는 앱"` | 부동산 도메인 추론 → O2O 패턴 교차 → 하이브리드 설계 |
| MVP 와이어프레임 | `"AI 튜터 앱 목업 만들어줘"` | 교육+AI 도메인 매칭 → 클릭 가능한 모바일 와이어프레임 HTML 산출 |

## 주요 기능

- **28개 도메인 패턴 DB** — 190+개 성공 앱을 4축(도메인, 비즈목표, 비즈모델, UX패턴)으로 분석
- **12개 진보 원칙** — 기존 앱을 초월하는 설계: 제로온보딩, AI-First개인화, 에이전트UI, 마이크로수익화 등
- **자동 도메인 매칭** — 키워드 테이블로 입력을 적합한 도메인에 매칭; 하이브리드 아이디어용 크로스도메인 블렌딩
- **4단계 파이프라인** — 입력 → 패턴 분석 → 서비스 블루프린트 → 와이어프레임 HTML, 최소한의 핑퐁
- **모바일 퍼스트 HTML 산출** — 탭 네비게이션, 한글 더미데이터, 브랜드 컬러 테마의 클릭 가능 프로토타입

## 연동 스킬

- **[biz-skill](https://github.com/jasonnamii/biz-skill)** — 설계 후 사업 전략 검증
- **[ui-action-designer](https://github.com/jasonnamii/ui-action-designer)** — 와이어프레임 후 개별 화면 상세 UI 설계
- **[hit-skill](https://github.com/jasonnamii/hit-skill)** — 히트 패턴 적용으로 engagement 강화
- **[design-skill](https://github.com/jasonnamii/design-skill)** — 산출물에 Apple 스타일 디자인 적용

## 설치

```bash
git clone https://github.com/jasonnamii/app-architect.git ~/.claude/skills/app-architect
```

## 업데이트

```bash
cd ~/.claude/skills/app-architect && git pull
```

`~/.claude/skills/`에 배치된 스킬은 Claude Code 및 Cowork 세션에서 자동으로 사용 가능합니다.

## Cowork Skills

25개 이상의 커스텀 스킬 중 하나입니다. 전체 카탈로그: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## 라이선스

MIT License — 자유롭게 사용, 수정, 공유 가능합니다.