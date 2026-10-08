# Industry gap

TRCA is not an official OWASP entry or MITRE technique. Pieces of it already live in three frameworks. The class still does not fit any one box.

## The argument

The case for naming the class does not wait for a published attack on a critical agentic service. Defenders can harden the allowance now.

1. **Name the classes.** Insider seat, Stolen key, Runaway agent, Agentic Service Degradation. One allowance, four classes.
2. **The wiring is already in production.** Coding seats, keys in apps, uncapped tool loops, and several agentic features on one model token are how these systems run today. See [sub-attacks.md](sub-attacks.md).
3. **Each class has an action now.** Cap the person and cut the seat with the leaver process. Keep the key out of the app. Cap the loop. Give the critical service its own token. See [controls.md](controls.md). Those actions are usable before anyone publishes an incident.
4. **The frameworks cover slices, and the field is moving.** T1496.004 covers the stolen key, including cost and a used-up quota. LLM06:2026 covers a missing cap. AML.T0034.002 covers coerced expensive tool calls. None of them covers abuse of a valid seat, or a shared token that degrades a critical service. Offense is already using AI to move faster, and the defense being bought is an agentic SOC on a finite allowance. One or more of the four classes can spend that allowance. The running record is [trade-winds.md](trade-winds.md). It is not a case. The missing slice should be named before a critical service is spent on purpose.

A contribution describes impact, preconditions, detections, and mitigations. It does not describe how to spend the meter.

## What exists today

### OWASP GenAI / LLM Top 10 (2026)

**LLM06:2026 Unbounded Consumption** (was LLM10:2025) is the closest *vulnerability*. It says the application failed to bound inference: cost, tokens, tool loops, reasoning, extraction.

That is necessary and not sufficient.

| LLM06 covers | LLM06 does not name |
|---|---|
| Missing spend and depth bounds on an LLM app | Abuse of a valid seat |
| Denial of Wallet as an effect | A shared model token that degrades a critical service |
| A missing cap on a loop | A separate allowance and a monthly limit per critical service, where the product allows that split. A new key per job is not the control. |

**Proposal toward OWASP:** keep LLM06 as the defect. Publish TRCA as an abuse / impact profile that AppSec and SecOps can share — including insider seats and prepaid investigators.

### MITRE ATT&CK

| Technique | What it is | Gap versus TRCA |
|---|---|---|
| [T1499](https://attack.mitre.org/techniques/T1499) Endpoint Denial of Service | Exhaust host or service resources so the service falls over | TRCA often leaves the app up |
| [T1496](https://attack.mitre.org/techniques/T1496) Resource Hijacking | Use victim compute for the attacker’s work (mining, spam, LLMJacking) | Motive is often *the attacker’s* workload, not emptying *your* investigator |
| [T1496.004](https://attack.mitre.org/techniques/T1496/004) Cloud Service Hijacking | Compromised SaaS used for the attacker’s resource-intensive work, including LLMJacking through a reverse proxy. The page lists significant cost, used-up service quotas, and an impact on availability as effects of that hijack. Read 6 Oct 2026. Created 25 Sep 2024. Last modified 15 Apr 2025. | Stolen key only when the procedure is that hijack. A public client key, a stolen login session, and a bill-only flood are not this procedure. It does not cover abuse of a valid seat or Agentic Service Degradation. |

T1496.004 has the right effect when a stolen credential is used to run the attacker’s work. The page itself says the victim can incur significant financial cost and use up service quotas. It also names LLMJacking. That is merit. It is not every bill, and it is not the whole class. A person who is still allowed in is not that procedure. Neither is a public client key, a stolen login session, or a critical service that degrades because it shares an allowance with other work.

**Proposal toward ATT&CK:** keep T1496.004 for compromised SaaS used for the attacker’s work, including LLMJacking. The open gap is abuse of a valid seat, and a shared allowance that degrades a critical service, while the application stays up. No new number is proposed here.

Agentic Service Degradation is not T1499. The application, and often the detector, stay up. What gets thin is the agentic feature.

### MITRE ATLAS

ATLAS already tracks cost abuse of AI services. Read on the techniques index, 6 Oct 2026, at [atlas.mitre.org/techniques](https://atlas.mitre.org/techniques):

- **AML.T0034 Cost Harvesting.** Drive a victim’s AI services beyond normal operating capacity to raise the cost. The page splits that into excessive queries, resource-intensive queries, and agentic resource consumption.
- **AML.T0034.000** Excessive Queries. A high volume of otherwise normal or low-complexity queries, to raise cost and load.
- **AML.T0034.001** Resource-Intensive Queries. Inputs crafted to cost more compute.
- **AML.T0034.002 Agentic Resource Consumption.** Coerce an agentic system into expensive tool calls that waste resources and consume an API budget. The page names prompt injection and tool-data poisoning as the way in, and gives abuse prompts as examples.

AML.T0034.002 is real, and it is the closest published ID to the runaway-agent class. The merit is the API budget and the tool-call fan-out. The gap is the procedure. The page describes an adversary coercing the agent. It does not describe abuse of a valid work seat. It does not describe a critical service that degrades because it shares a model token with other ordinary work.

**Proposal toward ATLAS:** keep AML.T0034.002 for coerced tool-call cost. Extend the parent so it also covers an authorized identity and a shared allowance. An investigator is the clearest case, not the limit of the class.

## Why a new class (not just a footnote)

Existing boxes assume one of these:

1. The attacker is outside and stole a key.
2. The attacker is trying to knock a host over.
3. The product forgot a rate limit.

TRCA adds facts those assumptions miss:

- The spender can be an employee who is still allowed in. That is abuse of a valid seat.
- The damaged object can be a critical agentic service, not a website.
- Request-rate limits are the wrong unit when one request can fan out into expensive reasoning and tools.
- Where the product allows it, the practical fix is a separate allowance and a monthly limit per critical service, plus a path that still runs when that allowance is spent. A new key per job is not that fix. On Microsoft 365 E5 and E7, Security Copilot inclusion is one monthly tenant allotment. A second API key does not split it.

Until OWASP and MITRE adopt language for that, this repository is the working name.

## What 2026 reporting already proved

CSA *LLMjacking Evolved* (20 June 2026), the Maps and Firebase to Gemini billing cluster, and CARBONATO (ThreatDown, with Security Affairs 25 Sept, BleepingComputer 24 Sept, and Dark Reading 28 Sept) are public evidence for Stolen key. Dark Reading with Forcepoint (21 Sept 2026) is an explainer for Runaway agent. It is not a Stolen key case. None of these is Insider seat, and none is Agentic Service Degradation. Full table: [public-evidence.md](public-evidence.md). Those two classes are still the gap. Agentic Service Degradation is a reasoned extension of published meters and of shared commercial agent pools, not an in-the-wild attack on a named critical service. There is no published case of someone spending a shared allowance on purpose until a named critical service could not start new work.

## What this is not

- TRCA is not LLM06. LLM06 is the hole in the product. TRCA is the abuse pattern.
- TRCA is not T1496.004. That ID is one class.
- MITRE has not published a SOC-quota technique.
- A framework contribution needs impact, preconditions, detections, and mitigations. It does not need a way to spend the meter.

## Suggested submission path

1. Cite this repository as the working definition.
2. Map each class to existing IDs (this page).
3. Draft an ATT&CK/ATLAS-style technique stub (impact, platforms, mitigations, detections) with no exploit recipe.
4. Contribute via OWASP GenAI working group comments and MITRE ATT&CK/ATLAS contribution processes.
5. Keep Agentic Service Degradation labeled as a reasoned extension until a public incident or a vendor post-mortem exists. The SOC investigator is the clearest case of that class, not a separate class.
