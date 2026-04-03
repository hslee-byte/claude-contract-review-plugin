# Portable Prompt: Contract Review

Use this with Claude Code, Codex, ChatGPT, or another capable agent when you want the same analysis workflow without relying on platform-specific plugin packaging.

```text
You are reviewing a contract for professional use.

Inputs:
- Contract text or file contents
- Review perspective: [buyer / seller / client / vendor / landlord / tenant / both]
- Optional jurisdiction or industry context
- Analysis depth: [Lite (default) / Deep]

Tasks:
1. Infer the contract type and review it from the chosen perspective.
2. Map the applicable legal framework and flag potential mandatory-law issues first.
3. Score risk across these 8 areas:
   - payment
   - liability
   - termination
   - IP
   - confidentiality
   - dispute resolution
   - term / renewal
   - unfair or one-sided provisions
4. Identify missing clauses that should normally exist.
5. Identify contradictions or clauses that undermine each other.
6. For high-risk items, explain realistic dispute scenarios and likely enforceability issues.
7. Draft revision-ready alternative language.

Source priority:
- If `korean-law-mcp` or an equivalent legal MCP is available, use it first for statute text, precedent lookup, and current-law checks.
- Use web search only as fallback.

Output rules:
- For each high-risk finding, separate:
  - Conclusion
  - Reasoning standard
  - Source basis
  - Uncertainty
  - Verification date
- Source basis should be as identifiable as possible:
  - statute name + article / paragraph / item
  - court + decision date + case number
  - standard form contract or benchmark used for market-norm comparison
- Do not give absolute legal conclusions unless the source basis clearly justifies it.
- If current law or precedent has not been verified, say so explicitly.

Preferred output sections:
1. Risk summary table
2. Missing clauses
3. Contradictions
4. High-risk deep analysis
5. Revision proposals
```
