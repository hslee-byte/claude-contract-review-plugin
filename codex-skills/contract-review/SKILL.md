---
name: contract-review
description: Review a contract from a chosen party perspective, map applicable laws, score risk across payment/liability/termination/IP/confidentiality/disputes/term/unfairness, detect missing or contradictory clauses, and produce revision-ready language with explicit reasoning standards, source basis, verification date, and uncertainty notes.
---

# Contract Review

Use this skill when the user wants clause-by-clause contract risk analysis from PDF text, pasted text, or a contract excerpt.

## Workflow

1. Read the contract and infer the contract type.
2. Ask or infer the review perspective:
   - seller / buyer
   - client / vendor
   - landlord / tenant
   - both sides
3. Identify applicable laws and potential mandatory-law issues first.
4. Score the contract across these areas:
   - payment
   - liability
   - termination
   - IP
   - confidentiality
   - dispute resolution
   - term / renewal
   - unfair or one-sided provisions
5. Detect:
   - missing clauses
   - internal contradictions
   - clauses that formally grant a right but practically neutralize it
6. Produce revision-ready wording for high-risk items.

## Output Rules

For each high-risk finding, separate:

- Conclusion
- Reasoning standard
- Source basis
- Uncertainty
- Verification date

When possible, make source basis identifiable:

- statute name + article / paragraph / item
- court + decision date + case number
- standard form contract or practical benchmark used for market-norm comparison

## Detailed Finding Template

Use this structure for high-risk clauses:

```text
[Clause / Topic]

Conclusion:
- What the risk is and why it matters

Reasoning standard:
- The legal or practical test used to assess the clause

Source basis:
- Statute / precedent trend / standard form / benchmark

Market norm comparison:
- What is typical and how this clause differs

Dispute scenario:
- What likely happens if the clause is enforced in a real dispute

Enforceability:
- Whether the clause is likely to be reduced, ignored, or challenged

Revision:
- Suggested wording

Revision rationale:
- Why the revised wording is more balanced or defensible

Uncertainty:
- What additional facts or current-law checks are still needed

Verification date:
- YYYY-MM-DD
```

## Constraints

- Do not present definitive legal advice.
- Phrase legal invalidity as a risk or likelihood unless the user explicitly asks for a stronger legal view and the source basis clearly supports it.
- Mandatory-law risks require identifiable legal support.
- Keep the final output practical and negotiation-ready.
