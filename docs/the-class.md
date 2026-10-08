# The class

## Definition

**Token Resource Consumption Attacks (TRCA)** is a working name. It is not an accepted standard yet. The definition is here so defenders can recognize the class before it is used in a live incident against their organization. The goal is to harden the systems, services, and workflows that spend AI.

A meter can be spent by abuse of a valid seat or by a stolen credential, until the bill spikes, the quota is gone, or a dependent agentic service degrades. The application may stay up. The vendor may also freeze the project. Health checks can stay green, because they are not watching the allowance.

Three facts sit under that:

1. The work is allowed inference. The seat still works, or the credential still works.
2. The scarce resource is prepaid model work: tokens, Security Compute Units, vendor credits. Not only CPU or bandwidth. A Security Compute Unit is a vendor meter. It is not the model token.
3. What fails can be the bill, a critical agentic service, or the cloud project if the vendor suspends it. The rest of the application can stay up.

## What TRCA is not

| Not this | Why |
|---|---|
| A break-in | Abuse of a seat that is still allowed, or use of a key that is still valid, is enough. No exploit is required. |
| An outage | Health checks can stay green. They are not watching the allowance. A vendor can still suspend the whole cloud project after a burn. That is blast radius on a shared project, not a packet flood. |
| Theft | Exfiltration is a different incident. The effect here is the bill, or a degraded service. |
| Prompt injection as the class | Injection can be one way in. The class is the meter. |
| OAuth or session-token theft as a different class | “Token” in TRCA is not an OAuth session. A stolen login that spends the model allowance is Stolen key. |
| TokenBreak | Tokenizer evasion. A different problem. |
| Tokenmaxxing | Spending an allowance the account already pays for, before the period ends. Not an attack. |

## How to label one incident

Label the incident with the class, then with the existing ID that covers only that slice.

| Layer | Question | What to say |
|---|---|---|
| Class | Which of the four? | Insider seat, Stolen key, Runaway agent, or Agentic Service Degradation |
| Existing ID | Which published name covers a slice? | OWASP LLM06:2026, ATT&CK T1496.004, ATLAS AML.T0034, or none. Insider seat has no ID. |
| Effect | What failed? | The bill spiked, or a critical service degraded |

A work-AI seat being “for legitimate work” does not remove LLM06. Unbounded Consumption is the missing cap. It is not the whole attack.

## Vocabulary

- **TRCA** — the working name for the whole pattern. Not an accepted standard yet.
- **Model token** — the key or credit pool one workflow spends. Not the billed token count, not a person’s login, and not a vendor meter such as a Security Compute Unit or a Google Security Token.
- **Tokenmaxxing** — not the attack. Spending an allowance the account already pays for, before the period ends. The goal is to use as much of that quota as the period allows. A high usage report is the same pattern. No critical service degrades.
- **Token Torching** — a public 2026 name for burning tokens while the model does allowed work. It names the bill. It does not name abuse of a valid seat, or a shared token that degrades a critical service.
- **Agentic Service Degradation** — several critical services share one model token. Spending the month degrades all of them. New work does not start, or it degrades, and the work falls back on the human queue.

## Why the class is needed

Each current name covers a slice:

- Denial of Wallet names the bill. It does not name abuse of a valid seat, and it does not name a degraded agentic service.
- Unbounded Consumption (OWASP LLM06:2026) names a missing cap. It does not name the whole attack.
- ATT&CK T1496.004 names compromised SaaS used for the attacker’s work, including LLMJacking, and it names cost and a used-up quota as impacts of that hijack. It does not cover abuse of a valid seat, a public client key, a stolen login session, or a shared model token.
- ATLAS AML.T0034.002 names coerced expensive tool calls that consume an API budget. It misses abuse of a valid seat, and it misses a shared token.

None of them, alone, covers a critical service that degrades because it shares a model token with other work. Until one does, the working name is TRCA.
