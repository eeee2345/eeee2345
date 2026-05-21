# Adam Lin

Maintainer of [Agent Threat Rules](https://github.com/Agent-Threat-Rule/agent-threat-rules) — an open MIT-licensed detection corpus for AI agent threats. Sigma for the agent surface.

Founder of [Panguard AI](https://panguard.ai) (Delaware C-Corp), the commercial product that operationalizes ATR for enterprises.

Based in Taipei.

[![ATR on npm](https://img.shields.io/npm/v/agent-threat-rules?label=agent-threat-rules%20%40npm&color=blue)](https://www.npmjs.com/package/agent-threat-rules)
[![Downloads](https://img.shields.io/npm/dm/agent-threat-rules?label=npm%20downloads%2Fmonth)](https://www.npmjs.com/package/agent-threat-rules)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/Agent-Threat-Rule/agent-threat-rules/blob/main/LICENSE)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19178002.svg)](https://doi.org/10.5281/zenodo.19178002)
[![GitHub stars](https://img.shields.io/github/stars/Agent-Threat-Rule/agent-threat-rules?style=social)](https://github.com/Agent-Threat-Rule/agent-threat-rules)

---

## What's in production

ATR rules are merged into the following external products, each verifiable as a public GitHub merge:

| Org | What landed | PR |
|---|---|---|
| Microsoft Agent Governance Toolkit | 287-rule production expansion | [microsoft/agent-governance-toolkit#1277](https://github.com/microsoft/agent-governance-toolkit/pull/1277) |
| Microsoft Agent Governance Toolkit | 15-rule PoC | [#908](https://github.com/microsoft/agent-governance-toolkit/pull/908) |
| Cisco AI Defense skill-scanner | Full ATR rule pack | [cisco-ai-defense/skill-scanner#99](https://github.com/cisco-ai-defense/skill-scanner/pull/99) |
| Cisco AI Defense skill-scanner | PoC | [#79](https://github.com/cisco-ai-defense/skill-scanner/pull/79) |
| MISP CIRCL misp-galaxy | Global threat-intel cluster | [MISP/misp-galaxy#1207](https://github.com/MISP/misp-galaxy/pull/1207) |
| MISP CIRCL misp-taxonomies | Rule-ID tagging vocabulary | [MISP/misp-taxonomies#323](https://github.com/MISP/misp-taxonomies/pull/323) |
| precize / Gen Digital Sage chain | Agent-Security-Regression-Harness | [precize/Agent-Security-Regression-Harness#74](https://github.com/precize/Agent-Security-Regression-Harness/pull/74) |
| precize Agentic-AI-Top10-Vulnerability | OWASP-Agentic mapping | [#14](https://github.com/precize/Agentic-AI-Top10-Vulnerability/pull/14) |

In review at upstream: NVIDIA garak, OWASP LLM Top 10, IBM mcp-context-forge, Meta PurpleLlama, promptfoo, Microsoft PyRIT.

---

## The Microsoft Copilot loop (2026-05-11)

On 2026-05-07, Microsoft Security Response Center disclosed two Semantic Kernel CVEs (CVE-2026-26030, CVE-2026-25592).

On 2026-05-11 at 06:07 UTC, Microsoft's Copilot SWE Agent autonomously opened [microsoft/agent-governance-toolkit#1981](https://github.com/microsoft/agent-governance-toolkit/issues/1981) with regression-test fixtures presuming ATR detection of those CVEs.

By 08:24 UTC the same day, [ATR v2.1.2](https://www.npmjs.com/package/agent-threat-rules) with rules `ATR-2026-00440` and `ATR-2026-00441` was merged, npm-published, and GitHub-released.

End-to-end CVE-disclosure to shipped-detection-rule: **2 hours 16 minutes**.

Honest caveat: coverage was partial. Two of four Copilot-generated fixtures matched the v2.1.2 canonical regex shape; the remaining two required deeper semantic work that landed in later versions. The point is the substrate-based velocity, not coverage completeness.

---

## Numbers

CI-locked in `stats.json`, drift-checked on every commit:

- 425 rules across 10 categories
- 96,096 wild-scanned production skills across OpenClaw, ClawHub, Skills.sh, Hermes
- 751 confirmed malicious skills in the corpus
- SKILL.md detection: 100% recall, 100% precision, 0.20% false positive (498 real-world samples)
- garak recall: 97.1%
- MCP precision 99.6%, recall 62.7% (recall gap honestly disclosed)

---

## Standards mappings

- OWASP Agentic Top 10: 10 of 10 categories mapped
- SAFE-MCP: 78 of 85 techniques mapped (91.8%)
- MITRE ATLAS: 100 of 113 techniques mapped
- Five Eyes 2026-05 AI agent joint guidance: mapped to ATR's 10 categories
- NIST AI RMF community OSCAL catalog: self-published at [Agent-Threat-Rule/ai-rmf-oscal-catalog](https://github.com/Agent-Threat-Rule/ai-rmf-oscal-catalog), Path 1 invitation received from NIST (not yet reviewed)
- Internet-Draft prepared for IETF SECEVENT WG

---

## Provenance and licensing

- MIT license on rules, code, and docs
- Zenodo DOI: [10.5281/zenodo.19178002](https://doi.org/10.5281/zenodo.19178002)
- Registered trademarks: ATR®, ATR-Certified™
- Fiscal sponsor for the open standard: Open Source Collective Inc. (501(c)(3), EIN 81-1567737, confirmed 2026-05-19)

---

## Contact

- Website: [panguard.ai](https://panguard.ai)
- Email: adam@agentthreatrule.org
- ATR org: [github.com/Agent-Threat-Rule](https://github.com/Agent-Threat-Rule)
