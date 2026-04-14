# app-architect

> 🇰🇷 [한국어 README](./README.ko.md)

**Domain-aware platform mockup builder. Feed it a business direction, and it pattern-matches against 190+ successful apps across 28 domains to produce a service blueprint and clickable wireframe HTML.**

## Prerequisites

- **Claude Cowork or Claude Code** environment

## Goal

Most app designs start from a blank canvas or copy a single competitor. app-architect flips this: it loads proven patterns from 28 industry domains (travel, fintech, e-commerce, AI/chatbot, pet, grocery, etc.) and layers 12 "beyond patterns" — design principles that surpass what existing apps do — to produce a differentiated service design and a working mobile wireframe in one shot.

## When & How to Use

Trigger it whenever you're sketching a new app or platform. Just describe what you want to build — a reference app ("something like Airbnb for pets"), a domain ("pet community platform"), or a problem ("help dog owners find nearby vets"). The skill asks up to 3 clarifying questions, then runs a 4-phase pipeline: domain matching → pattern analysis + beyond-pattern application → service blueprint → wireframe HTML output.

## Use Cases

| Scenario | Prompt | What Happens |
|---|---|---|
| New platform idea | `"펫 커뮤니티 앱 설계해줘"` | Matches pet domain, loads 6 app patterns, applies beyond-principles, outputs blueprint + HTML |
| Reference-based design | `"에어비앤비 같은 숙박 앱"` | Matches accommodation domain, analyzes Airbnb patterns, designs improved version |
| Problem-driven design | `"동네 빈집 문제 해결하는 앱"` | Infers real-estate domain, cross-references O2O patterns, outputs hybrid design |
| MVP wireframe | `"AI 튜터 앱 목업 만들어줘"` | Matches education + AI domains, outputs clickable mobile wireframe HTML |

## Key Features

- **28-Domain Pattern DB** — 190+ successful apps analyzed across 4 axes: domain, business goal, business model, UX patterns
- **12 Beyond Patterns** — Design principles that surpass existing apps: zero onboarding, AI-first personalization, agent-driven UI, micro-monetization, and more
- **Auto Domain Matching** — Keyword table maps any input to the right domain(s); cross-domain blending for hybrid ideas
- **4-Phase Pipeline** — Input → Pattern Analysis → Service Blueprint → Wireframe HTML, with minimal back-and-forth
- **Mobile-First HTML Output** — Clickable prototype with tab navigation, real Korean dummy data, and brand color theming

## Works With

- **[biz-skill](https://github.com/jasonnamii/biz-skill)** — Business strategy validation after design
- **[ui-action-designer](https://github.com/jasonnamii/ui-action-designer)** — Detailed single-screen UI design after wireframe
- **[hit-skill](https://github.com/jasonnamii/hit-skill)** — Apply hit patterns to boost engagement
- **[design-skill](https://github.com/jasonnamii/design-skill)** — Apple-style visual polish on outputs

## Installation

```bash
git clone https://github.com/jasonnamii/app-architect.git ~/.claude/skills/app-architect
```

## Update

```bash
cd ~/.claude/skills/app-architect && git pull
```

Skills placed in `~/.claude/skills/` are automatically available in Claude Code and Cowork sessions.

## Part of Cowork Skills

This is one of 25+ custom skills. See the full catalog: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## License

MIT License — feel free to use, modify, and share.