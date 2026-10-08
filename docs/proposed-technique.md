# Proposed technique stub (not official)

This page is a draft shape for a future ATT&CK or ATLAS contribution. It is **not** an assigned MITRE ID.

## Name

Metered AI Allowance Exhaustion (working title)  
Also known as: Token Resource Consumption Attack (TRCA)

## Tactic

Impact (availability of a *control* or a *budget*, not always of a host)

## Platforms

SaaS, IaaS, identity-bound enterprise AI assistants, agentic SOC products

## Description

Adversaries, or authorized users with hostile intent, cause a victim’s prepaid model, credit, SCU, or vendor-credit allotment to be spent on allowed inference and tool work until cost, quota, or a dependent function (investigation, support, coding) degrades. The target application often remains available. Request-count limits may not bind the cost of a single agentic task.

## Procedure examples (non-operational)

- A departing employee uses a still-valid work-AI seat to consume the team allowance.
- A leaked application key is used to call a high-tier model until the monthly cap or bill threshold is hit.
- An agentic workflow is driven into long tool chains or long hidden reasoning so one ticket costs far more than a normal ticket.
- High volumes of work a SOC is supposed to inspect can consume a prepaid investigator, leaving classic detections up and paid triage thin. No published case.

## Mitigations

- Insider seat: a monthly cap per person and per tool. Revoke the work-AI seat with VPN and email when someone gives notice.
- Stolen key: do not hardcode the model key. A public client key gets its own project. Alert on the allowance, not only on uptime.
- Runaway agent: cap tool calls, the loop, and the spend per run. Do not treat a new key per job as the control.
- Agentic Service Degradation: where the product allows it, one allowance and one monthly limit per critical service. Cap the tool calls. Group repeated events into one investigation, with a ceiling on how much context that investigation can grow. A path that still runs, and a human queue that knows it is taking the work, when that allowance is spent. A real attack can arrive while services are degraded. That is a possibility, not a published case.
- Alert on spend by identity and by service.

## Detections (conceptual)

- Sudden spend by one identity versus its baseline.
- One service consuming a shared allowance that also funds a higher-severity service.
- Agent runs with abnormal tool-hop or reasoning-token counts.
- Investigator throttle or 429/quota events correlated with a rise in low-fidelity work.

## Related existing IDs

- OWASP LLM06:2026 Unbounded Consumption (defect)
- ATT&CK T1496.004 Cloud Service Hijacking. Compromised SaaS used for the attacker’s work, including LLMJacking. It does not cover abuse of a valid seat, a public client key, a stolen login session, or a shared allowance.
- ATT&CK T1499 Endpoint DoS, only if the host falls over.
- ATLAS AML.T0034 Cost Harvesting, and AML.T0034.002 Agentic Resource Consumption. Coerced tool-call cost. It does not cover abuse of a valid seat. It does not cover a shared allowance.
- CSA, June 2026, LLMjacking Evolved. In-the-wild stolen inference. Stolen key only.
- Dark Reading / Forcepoint, September 2026. Denial of Wallet as a name for the bill, plus fan-out and reasoning loops. An explainer for Runaway agent. Not a Stolen key invoice.

## Contribution notes

Submit through official MITRE and OWASP processes. Do not attach exploit recipes. Keep the fourth class, Agentic Service Degradation, labeled as a reasoned extension until a public incident exists. Do not assign it a number.
