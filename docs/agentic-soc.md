# Agentic SOC

This page is one example of **Agentic Service Degradation**. It is not the whole class, and it is not a published incident. When the paid investigator hits its limit, new agentic investigations do not start. That is not “the SOC went offline.”

An Agentic SOC uses a prepaid investigator: an AI agent that triages, enriches, and writes up alerts. That investigator is metered as a monthly or daily allowance, not as unlimited electricity.

If every noisy event can start a paid look, an adversary does not have to break detection. They only have to make that look spend itself.

## Accurate claim

EDR and SIEM rules usually stay up on a different bill. What can throttle is machine-speed investigation. People inherit the queue. That is weaker detection if the organization staffed as if the agent was the SOC.

The paid investigator can hit its limit. That is not “the SOC goes offline.”

## Published meters

| Vendor | Unit | What happens at the bound |
|---|---|---|
| Microsoft Security Copilot, provisioned | Security Compute Units, billed per hour | Requests stop when provisioned units run out, unless overage or another capacity is available. |
| Microsoft Security Copilot, Microsoft 365 E5 and E7 inclusion | A monthly tenant allotment of Security Compute Units. Not an API key, and not an hourly pool. | Microsoft’s inclusion FAQ: usage beyond the allotment will be throttled at a future date. Pay-as-you-go is described for that later date, with 30 days’ notice. Read 7 Oct 2026. |
| Google SecOps Agentic SOC | Security Tokens | Per-tenant activation, built-in limits against runaway agent loops, admin daily ceilings. Complimentary tokens reset and do not roll over. |
| CrowdStrike Charlotte AI | Monthly credits | Cap sized to endpoints. Unused credits do not carry over. Per-agent caps. |
| Elastic | Per-agent tokens | Published accounting so teams can measure and specialize agents. |
| Alibaba Cloud Agentic SOC | Credits | After upfront credits die, new work can block unless overflow pay-as-you-go was chosen. |

Sources are listed in [references.md](references.md).

## What to separate

- The investigator’s allowance is not the helpdesk allowance, and not the coding-agent allowance, where the product lets you split them.
- High-severity work keeps a monthly slice that other work cannot spend, where the product has a slice. Included E5 and E7 Security Copilot capacity is one tenant allotment. A second API key does not create a second one.
- Group repeated events into one investigation, with a ceiling on how much context that investigation can grow. Grouping does not replace a separate allowance.
- When the investigator hits its cap, a written non-AI playbook still runs.

## Not a published case

Attackers already throw noisy tickets, floods, and junk work at human defenders. The same pile can spend an agentic investigator, because each item can start paid AI work or grow the context that investigator has to read.

This is an extrapolation. It uses how human defenders are already loaded, plus the published fact that these investigators are finite. It is not a published case of an emptied agentic SOC.

## What degradation looks like

When the investigator’s model token has spent its pay-period allotment, agentic investigations stop starting. Work already in flight may finish. The human queue then takes what the agent was supposed to look at.

A real attack can arrive while services are degraded. That is a possibility. It is not a published case.

Vendor docs already describe the stop:

- Google SecOps: if you only have included Security Tokens and they run out, you will not be able to start new agents. Agents already started run to completion. Paid tokens then overage unless an admin set a limit.
- Microsoft Security Copilot, provisioned capacity: when provisioned Security Compute Units run out and no other capacity is available, requests stop. The “next hour” clock is this provisioned path, not the E5 and E7 monthly allotment.
- Microsoft Security Copilot, E5 and E7 inclusion: usage beyond the monthly allotment will be throttled at a future date. That throttle is not documented as live.

Classic EDR and SIEM rules usually stay up on a different bill. What stops starting is the agentic investigation, not the whole detector.

## Two other markets already on a finite agent meter

Same class. Not a published TRCA incident. The impact shows up if one token or credit pool is shared.

- **IT incident agents.** ServiceNow Now Assist and Otto for incident management consume a finite Assist pool. Interactive prompts, agent workflows, and non-production instances can draw the same pool as production. A password-reset bot on that pool can spend the period allotment the incident agent needed. New incident assists can then stop or need a top-up. The human queue can take major incidents. No vendor has published that stop.
- **Customer and case agents.** Salesforce Agentforce meters Flex Credits in a Digital Wallet. A public help agent and an internal case or fraud workflow on one wallet share one period allotment. Public resolutions can spend the credits the internal agent needed. Case work can degrade while the website stays up. That is a way the pool can fail. It is not a published incident.

Where the product allows it, the critical service gets its own allowance. A higher-tier model is a cost choice. It burns a reserved allotment faster. It is not a separate pool.

CARBONATO and CSA *LLMjacking Evolved* show stolen keys already paying for attacker-side agents. If the defender’s investigator shares a monthly allowance with helpdesk or a public app, that spend can land on the investigator’s token. That is the scene. It is not a published case of an investigator quota being spent on purpose. See [public-evidence.md](public-evidence.md).
