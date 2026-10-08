# Four classes

Same allowance. Different class.

Each class below is four things: what it is, where that pattern already shows up in agentic systems, what to do about it on systems that are running now, and which published framework ID covers only a slice. The actions are not a product purchase. They do not wait for a named incident.

## Insider seat

A login that still works, used to spend the company AI allowance. No jailbreak is required. The person is supposed to use the coding agent, the internal assistant, or the company chat.

**In use today.** Those seats are already how firms ship agentic work: Copilot, coding agents, and internal assistants on a shared company allowance. The leaver process usually cuts VPN, email, and the badge. A still-valid AI seat is the exposure to close. Nothing on file shows that offboarding left one on. Large work-AI bills, including a Microsoft spreadsheet reported in August 2026, are the adjacent fact. Motive is not always sabotage. Tokenmaxxing — spending an allowance the account already pays for, before the period ends — is the same meter and is not this class.

**Action today.**

- Put a monthly cap on each person and each AI tool.
- When someone gives notice, cut the AI seat in the same leaver process as VPN and email. Do not wait for the last day.
- Treat a high bill as a question about the seat, not as proof of sabotage.

**Framework slice.** No catalog ID covers this class. OWASP LLM06:2026 names a missing cap, not the motive. ATT&CK T1496.004 is a compromised service, not a person who is still allowed in.

## Stolen key

A leaked or hardcoded key spends the model. The application can stay up. The invoice is the incident. Sometimes the vendor then suspends the whole project.

**In use today.** Agentic apps and mobile clients already call a model with a key that lives in the app, in a repo, or on a developer machine. A Maps or Firebase key in the same cloud project has been accepted by Gemini. A poisoned editor extension is one way that key leaves the machine. It is not, by itself, an AI invoice. Stolen keys are already paying for attacker-side agents. See CSA, 20 June 2026, and CARBONATO, September 2026, in [public-evidence.md](public-evidence.md).

**Action today.**

- Do not hardcode the company model key into an application, and do not leave it as the only copy on a developer machine.
- Do not share that key with backend agents and with company chat.
- A public client key gets its own cloud project. A second key in the same project still shares the cap and the suspension.
- Alert on the invoice and the allowance, not only on whether the app answers.

**Framework slice.** ATT&CK T1496.004 is compromised SaaS used for the attacker’s work, including LLMJacking. Cost and a used-up quota are impacts of that hijack. A public client key and a stolen login session can still be Stolen key here. They are not automatically that technique.

## Runaway agent

One request. No ceiling. Follow-up tool calls and hidden thinking become a second bill. A limit that only counts requests misses it.

**In use today.** Coding agents, support bots, research agents, retrieval apps, and workflow runners already fan one request out into many model calls. Dark Reading with Forcepoint, September 2026: the tool chain, the reasoning loop, and a growing chat can drive the cost, and one request can still look normal. That piece is an explainer. It is not a Stolen key invoice. A new key for every job is not how these products are sold, and it is not feasible as the fix. Two first-person stalls, neither an attack and neither Agentic Service Degradation: OpenAI Developer Community, 20 September 2026, one scan spent a fresh weekly Codex allowance in about 44 minutes and the next worker could not start. Google AI Developers Forum, 30 September 2026, agent runs burned a project tokens-per-minute cap while the request counts still looked fine. A weekly window and a per-minute cap are not several critical services sharing one month.

**Action today.**

- Cap the tool calls, the loop, and the spend, per agent.
- Count more than the request. Hidden thinking is part of the bill.
- Do not plan on minting a new key for every job.

**Framework slice.** OWASP LLM06:2026 names the missing cap. ATLAS AML.T0034.002 names an adversary coercing expensive tool calls, often by prompt injection or poisoned tool data. A loop on work the company already asked for is the same cost shape. It is not the same procedure.

## Agentic Service Degradation

Several critical services share one model token. Spending the month degrades all of them. New work does not start, or it comes back shorter and thinner, and the work falls onto the human queue that agent had been clearing. The rest of the application can stay up.

**In use today.** Some products meter several agentic features from one pool. That pool is not always an API key. Microsoft 365 E5 and E7 Security Copilot inclusion is one monthly tenant allotment of Security Compute Units. It is not a key a team can hand to one service, and a second API key does not create a second inclusion pool. Microsoft’s inclusion FAQ says usage beyond that allotment will be throttled at a future date, with 30 days’ notice before pay-as-you-go. Provisioned Security Compute Units are a different clock: they are billed per hour, and requests stop when that capacity runs out unless overage or another capacity is available. Google SecOps Security Tokens are a per-tenant balance, not an API key. ServiceNow Assist and a Salesforce wallet can be shared by more than one workflow. An agentic SOC investigator is the clearest example of what a shared allowance can degrade. It is not the only one. No vendor has published an attacker spending one of these pools on purpose.

**Action today.**

- List every agent and which allowance it spends.
- Give the critical service its own allowance where the product allows a separate key, wallet, or pool, and a month nobody else can spend. Company chat, the helpdesk, and a public bot get a different allowance. Where the vendor does not allow that split, say so. Do not mark a second API key as if it had created a second Security Compute Unit pool.
- Cap the tool calls.
- Group repeated events into one investigation, with a ceiling on how much context that investigation can grow.
- Watch that allowance. A green health check is not watching it. Write down what the human queue does when that token is spent.

**Framework slice.** No catalog ID. T1496.004 is a compromised service. AML.T0034.002 is coerced tool-call cost. Neither is a shared token across services the company meant to run. This class is a reasoned extension of published meters. It is not a published attack on a named investigator. The action does not wait for that incident. The meters are already in production.

## What the four actions have in common

None of them is a new tool. List the agents. Keep the key out of the app. Cap the loop. Give the critical service its own allowance where the product allows it. Cap the tool calls. Group repeated events into one investigation. The checklist is [controls.md](controls.md).

## Scope test

A feature is in scope if it is agentic, or augmented by an agent workflow, and it uses a model token that other features can also spend.

| Service | Why it is in scope |
|---|---|
| SOC / detect | A critical service. New investigations stop when the allowance is spent. |
| Support and helpdesk | Staff or public chat on a company token. |
| Coding agent | Seats and repo-wide agents on a company allowance. |
| Retrieval | One question fans out into many model calls. |
| Workflow agent | Automation on the same company limit. |
| Customer-facing agent | User traffic billed to the company. |
