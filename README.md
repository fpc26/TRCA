# Token Resource Consumption Attacks (TRCA)

**Status:** a proposed class. Not an official OWASP entry, MITRE technique, or vendor advisory.  
**Not:** exploit documentation.

This repository is the home for the talks at BSides Philly, December 2026, and FS-ISAC, March 2027. Any cyber defender can use it to learn the four classes and harden the systems, services, and workflows that spend AI, before a class is used in a live incident against their organization.

TRCA names a pattern that already exists in pieces and is not yet treated as one class:

> A meter can be spent by abuse of a valid seat or by a stolen credential, until the bill spikes, the quota is gone, or a dependent agentic service degrades. The application may stay up. The vendor may also freeze the project.

Four classes, one allowance: Insider seat, Stolen key, Runaway agent, and Agentic Service Degradation. An agentic SOC investigator is the clearest case of the fourth class, not the whole class. The same pattern applies to any AI feature that shares an allowance with a service that has to stay up.

The pages below are the definition, the evidence, and the controls. They do not include a method for driving a meter. There is not yet a published case of an attacker spending a named agentic investigator on purpose. The controls do not wait for that case.

## Read in this order

| Page | What it is |
|---|---|
| [The class](docs/the-class.md) | The definition, what TRCA is not, and how to label one incident. |
| [Four classes](docs/sub-attacks.md) | Abuse of a valid seat, a stolen or hardcoded key, a runaway agent, and a shared allowance that degrades a critical service. |
| [Industry gap](docs/industry-gap.md) | What OWASP, ATT&CK, and ATLAS already name, and what they still miss. |
| [Controls](docs/controls.md) | The hardening order for systems that are already running. |
| [Agentic SOC](docs/agentic-soc.md) | The published investigator meters, and what a spent allowance does to new investigations. |
| [Public evidence](docs/public-evidence.md) | Which 2026 reports are cases, which are not attacks, and which numbers are not used. |
| [Trade winds](docs/trade-winds.md) | Each public report, dated and aligned to the four classes. |
| [Timeline](https://fpc26.github.io/TRCA/timeline/) | Those events in date order. |
| [References](docs/references.md) | Outlet, date, and URL for each source. |
| [Technique stub](docs/proposed-technique.md) | A draft mapping for ATT&CK or ATLAS. Not an assigned ID. |

## Vocabulary

| Word | Meaning |
|---|---|
| **TRCA** | A meter spent by abuse of a valid seat or by a stolen credential, until the bill spikes, the quota is gone, or a dependent agentic service degrades. The application may stay up. The vendor may also freeze the project. |
| **Meter** | The allowance that gets spent: the bill, the quota, or the shared pool. The class is that spend. A health check is not a meter. A Security Compute Unit is one vendor’s meter, not the name of the class. |
| **Abuse of a valid seat** | Insider seat. A login that still works, used to spend the company AI allowance. No break-in is required. |
| **Tokenmaxxing** | Not the attack. Spending an allowance the account already pays for, before the period ends. No critical service is degraded. |
| **Agentic Service Degradation** | Several critical services share one model token. Spending the month degrades all of them. New work on the important service does not start, or it comes back thinner, and the work falls back on the human queue. |
| **Model token** | The key or credit pool one workflow spends. Not the billed token count, not a person’s login, and not a vendor meter such as a Security Compute Unit or a Google Security Token. |

## What this asks of the frameworks

- **OWASP LLM06:2026** names a missing cap on inference. It does not name abuse of a valid seat, and it does not name a shared model token that degrades a critical service.
- **MITRE ATT&CK T1496.004** names a compromised cloud service, including LLMJacking, and it names cost and a used-up quota. It does not name abuse of a valid seat, and it does not name a shared model token.
- **MITRE ATLAS AML.T0034.002** names an adversary coercing expensive tool calls that consume an API budget. It does not name abuse of a valid seat, and it does not name one model token shared across services.

None of those bodies has accepted TRCA. The notes here are a proposal.

## Keeping it current

The trade-wind log and the evidence page are the record. The chronology is published at [fpc26.github.io/TRCA/timeline](https://fpc26.github.io/TRCA/timeline/). It is compiled from those two documents.

## License

Informational content is offered under [Creative Commons Attribution 4.0](LICENSE). Cite **Token Resource Consumption Attacks (TRCA)** if you reuse it.

## Disclaimer

This is an awareness proposal. It is not an official OWASP entry, a MITRE technique, or a vendor advisory. There is no published case of an attacker spending a named agentic investigator on purpose. Two first-person stops are on file, and neither is an attack: OpenAI Developer Community, 20 September 2026, and the Google AI Developers Forum, 30 September 2026. Classic detections usually stay on a different bill. This repository does not claim a SOC went offline.
