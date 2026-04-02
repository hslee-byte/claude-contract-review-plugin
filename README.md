# Contract Review — AI 계약서 리스크 분석

> [한국어](#한국어)

A Claude Code plugin that analyzes contracts clause-by-clause. Upload a contract file (PDF, text, or paste), and get structured risk analysis with revision suggestions. Built for lawyers, accountants, and business professionals.

## What It Does

```
Contract file → Legal framework mapping → Risk scoring → Missing clauses → Contradictions → Revision suggestions
```

### 6-Phase Analysis

| Phase | What happens |
|---|---|
| **0. Read & Context** | Auto-detect contract type, ask which party's perspective |
| **1. Legal Framework** | Map applicable laws, flag mandatory provision violations (⚫) |
| **2. Risk Scoring** | Score 8 risk areas with market-standard benchmarks |
| **3. Gap & Contradiction** | Find missing clauses + internal contradictions between articles |
| **4. Deep Analysis** | Dispute scenarios, enforceability, specific revision wording |
| **5. Output** | Risk summary / Revision table / Legal memo / Negotiation checklist |

### Risk Levels

| Level | Meaning |
|---|---|
| 🟢 Low | Within market norms, acceptable |
| 🟡 Medium | Negotiation recommended |
| 🔴 High | Immediate revision needed |
| ⚫ Illegal/Void | Potential mandatory law violation |

### 8 Risk Areas

1. **Payment** — timing, late interest, advance payment
2. **Liability** — scope, cap, indemnification
3. **Termination** — grounds, notice period, penalties
4. **IP** — ownership, usage scope, derivatives
5. **Confidentiality** — scope, duration, breach penalties
6. **Dispute Resolution** — jurisdiction, arbitration
7. **Term/Renewal** — auto-renewal, notice period
8. **Unfair Terms** — unilateral changes, excessive penalties, imbalanced liability

## Install

```bash
claude plugin add hslee-byte/claude-contract-review-plugin
```

## Usage

```
/contract-review /path/to/contract.pdf
/contract-review
```

When run without arguments, you'll be asked how to provide the contract (file path, paste, or auto-find).

## Output Options

After analysis, choose your format:

1. **Risk Summary Table** — 1-page executive overview
2. **Revision Proposal** — Original vs. suggested wording side-by-side
3. **Legal Review Memo** — Internal report with legal basis and dispute scenarios
4. **Negotiation Checklist** — Pre-meeting preparation with concede/hold markers

## Safety

- Every output starts with: "⚠️ AI-assisted review. Final judgment must be confirmed with a legal professional."
- Never makes definitive legal conclusions — presents possibilities with legal basis
- Contract text and party information are never stored or memorized

---

## 한국어

계약서 파일(PDF, 텍스트)을 넣으면 조항별 리스크 분석 + 수정 제안을 해주는 Claude Code 플러그인. 변호사, 회계사, 사업가를 위해 만들었습니다.

### 분석 흐름

```
계약서 입력 → 관련 법령 매핑 → 8대 영역 리스크 스코어링 → 누락 조항 체크 → 조항 간 모순 검토 → 수정 제안
```

### 특징

- **관련 법령 자동 매핑** — 계약 유형에 따라 적용 법령과 강행 규정 식별
- **⚫ 위법/무효 등급** — 강행 규정 위반은 일반 리스크와 별도 표시
- **누락 조항 체크** — "있어야 하는데 없는 조항" 검출
- **조항 간 모순 검토** — 조항 A가 조항 B를 사실상 무력화하는 경우 검출
- **시장 관행 대비** — "이 조건이 업계에서 통상적인지" 코멘트
- **분쟁 시나리오** — "이 조항대로 가다가 터지면 어떻게 되는가" 시뮬레이션
- **집행 가능성** — "법원에서 실제로 인정될 가능성" 판단 (판례 경향 포함)

### 설치

```bash
claude plugin add hslee-byte/claude-contract-review-plugin
```

### 사용법

```
/contract-review 계약서.pdf
/contract-review
```

인자 없이 실행하면 입력 방식을 선택할 수 있습니다 (파일 경로 / 텍스트 붙여넣기 / 폴더에서 찾기).

### 결과물 형식

분석 완료 후 선택:

1. **리스크 요약 테이블** — 보고용 1장짜리
2. **수정 제안서** — 원문 vs 수정안 대조표 (누락 조항 추가 제안 포함)
3. **검토 의견서** — 내부 보고용 (법령 근거, 분쟁 시나리오 포함)
4. **협상 포인트** — 미팅 전 체크리스트 (양보 가능/불가 구분)

### 리스크 등급

| 등급 | 의미 |
|---|---|
| 🟢 낮음 | 시장 관행 내, 적정 |
| 🟡 중간 | 협상 권고 |
| 🔴 높음 | 즉시 수정 필요 |
| ⚫ 위법/무효 | 강행 규정 위반 가능성 |

### 안전장치

- 모든 결과물 상단에 "⚠️ AI 보조 검토입니다. 최종 판단은 반드시 법률 전문가와 확인하세요." 표시
- 확정적 법률 판단을 내리지 않음 — 가능성과 법적 근거를 제시
- 계약서 원문, 당사자 정보는 절대 기억/저장하지 않음

## License

MIT
