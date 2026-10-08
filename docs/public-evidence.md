# Public evidence (what is proven vs what is still a gap)

Retrieved through 7 October 2026. First-person bills are cited as *reported*, not as audited shutdowns.

## Proven: Stolen key

A production key meant for Maps, Firebase, or a mobile SDK was accepted by Gemini in the same Google Cloud project. Outsiders spent the victim’s inference bill. In several reports Google then suspended the whole project.

| Report | What that outlet printed | Use as |
|---|---|---|
| Tom’s Hardware, 4 Mar 2026. The Register, 3 Mar 2026, is the same bill. | $82,314 in 48 hours, against about $180 a month. The owner said bankruptcy if the bill was collected. | Stolen key. Reported bill. “If collected” stays in the sentence. |
| Cybernews, 13 May 2026, Colavo Ground | About $67,000 in 19 hours on a 2016 Firebase Android key | Named firm. Reported bill. |
| Cybernews, 13 May 2026 | Spain Maps key €36,800. Norway 2017 maps project about $7,500. | Legacy public keys. Reported figures from that article. |
| The Register, 13 May 2026 | $10,138 in minutes. | Reported charge. A budget alert is not the same thing as a hard quota. |
| Truffle Security, Feb–Jun 2026 | About 3,000 exposed keys in Common Crawl. Google later rejected unrestricted keys for Gemini (19 Jun 2026). | Exposed keys. This row is not a dollar amount. The $82,314 stays on the Tom’s Hardware line. |
| Google AI forum / RepoRank | €54,000 in 13 hours after Firebase AI Logic | Reported by that post. Budget alerts lagged. |
| r/startups and r/googlecloud, Sep 2026 | About $3,000 to $4,000 on a Maps key, then project suspension froze the app and customer photos | Bill plus a vendor fail-closed. First person. |

A recap that cites unnamed forum threads, including weekend and student figures with no outlet of their own, is not a case on this page.

Google’s June–September 2026 move to reject unrestricted standard keys for Gemini is official recognition that the old “keys are not secrets” design was a billing vector.

A public Maps key and the expensive model should not share a project. A different key in a different project, and a quota that stops the spend. A second key in the same project still shares the quota and the suspension.

## Citations that name an outlet and a period

Dollar amounts below are printed only with the source on the same line.

- **$82,314 / 48 hours** — Tom’s Hardware, 4 Mar 2026. The Register, 3 Mar 2026, TechSpot, 2 Mar 2026, and Techzine, 4 Mar 2026, are the same bill. The key was used 11–12 February. No new victim.
- **About $67,000 / 19 hours** — Cybernews, 13 May 2026, Colavo Ground.
- **Project freeze after a reused key** — first-person Google Cloud and r/startups threads, Sep 2026. Same pattern on the Google AI Developers Forum.
- **Maps or Firebase key reused for Gemini** — Truffle Security, and The Register, 13 May 2026.
- **Stolen keys fund attacker gateways** — CSA *LLMjacking Evolved*, 20 Jun 2026. CARBONATO, ThreatDown, reported by Security Affairs, 25 Sep 2026.
- **Stolen Claude sessions consumed usage** — BleepingComputer, 30 Aug 2026. The Register, 31 Aug 2026, is the same story. Infostealer malware copied Claude login sessions, and a bad actor used them to consume paid usage. Anthropic signed affected users out, removed saved payment methods, and refunded charges it identified as unauthorized. No dollar amount. Login sessions, not API keys. https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-warns-infostealer-malware-is-hijacking-claude-sessions-to-drain-usage/
- **Shared allowance, next job cannot start** — OpenAI Developer Community, 20 Sep 2026. One security scan spent a fresh weekly Codex allowance in about 44 minutes. The next worker could not start. First person. Not an attack. https://community.openai.com/t/fresh-weekly-codex-work-allowance-exhausted-in-44-minutes-by-security-scan-worker-fan-out/1399277
- **Shared project cap, counters still look fine** — Google AI Developers Forum, 30 Sep 2026. Agent runs burned the project tokens-per-minute cap. Request counts still looked fine, and the UI said the model was unlimited. Another key in that project would not have helped. Not an attack. https://discuss.ai.google.dev/t/the-real-cause-behind-ai-studio-build-quota-exceeded-the-agent-burns-your-projects-tpm-and-google-stays-silent/186027

## Proven: stolen inference as attacker infrastructure

| Report | What it shows |
|---|---|
| CSA, 20 Jun 2026, *LLMjacking Evolved*. Sysdig, 17 Jun 2026, is the lab post. A second CSA note, 26 Jun 2026, dates the observation to 12–14 June. | Stolen victim inference used as an offensive reasoning engine. Neither note adds a new victim or a new dollar amount. |
| Security Affairs, 25 Sep 2026, CARBONATO (ThreatDown research) | Botnet steals LLM keys as priority loot and funds its **own** LLM gateway for an installed agent |
| BleepingComputer, 24 Sep 2026; Dark Reading, 28 Sep 2026 | Same CARBONATO research, second outlets. Exposed Docker hosts, an implanted agent, AI API keys prioritized over other secrets. Does not add a new victim-bill figure and does not describe a SOC |
| CSA shadow-relay note, Jul 2026 | Underground resale of abused LLM credentials. Some of that resale is described as Denial of Wallet against exposed chatbots. |
| FortiGuard Labs, 3 Sep 2026, [Someone Else Is Using Your AI](https://www.fortinet.com/blog/threat-research/someone-else-is-using-your-ai) | A leaked long-lived AWS IAM key with administrator access was used to create a user, subscribe to foundation models, and invoke them. The lab says that generated inference charges on the victim account. No victim is named. No dollar amount is given for this incident. Hackread, 4 Sep 2026, is a second outlet. |

That is LLMJacking, which is Stolen key, feeding attacker agents. It is not a published case of someone spending a shared allowance on purpose until a named critical service could not start new work.

## Proven: agent is the new target (adjacent, not TRCA)

Security Affairs, 21 Sep 2026, *The Target Is No Longer the Model. It’s the Agent.* Poisoned skills, injection, tool hands. Maps to ATLAS. No spent allowance. Not a TRCA incident. Logged as direction in [trade-winds.md](trade-winds.md).

## Still a gap: insider motive and Agentic Service Degradation

- Abuse of a still-valid work seat is still thinly documented. The spreadsheet below is adjacent. It is not a hostile case.
- No public campaign that a CrowdStrike, Microsoft, or Google SecOps investigation quota was spent until the paid look stopped. That is one case of the fourth class, not the definition of it.
- Two first-person stops are on file, and both can be opened. OpenAI Developer Community, 20 Sep 2026: one scan spent a fresh weekly allowance in about 44 minutes, and the next worker could not start. Google AI Developers Forum, 30 Sep 2026: agent runs burned a shared project cap while request counts still looked fine. Neither is an attack. Neither is a named company.
- Shared bills plus stolen-key attacker agents are the scene, not the case study.
- ServiceNow Now Assist / Otto and Salesforce Agentforce are published finite pools. They show the class. They are not published TRCA incidents.

Agentic Service Degradation is not documented in the wild. The stolen-key cluster is the table above.

Direction that is not a case is in [trade-winds.md](trade-winds.md): Token Torching, the Kaspersky Denial-of-Wallet note, the Security Affairs piece on the agent as the target, the ZDNET LLMjacking note, the published investigator meters, and Dark Reading, 5 October 2026. Cases stay on this page.

## Adjacent, not a hostile case: large work-AI bills

TechRadar (27 Aug 2026) and The Next Web (26 Aug 2026) reported a voluntary Microsoft employee spreadsheet, on the order of 350 entries. The median AI spend in that window was about $300. One Customer and Partner Solutions figure was $28,000 over 28 days. Entries were voluntary and self-reported.

Large individual work-AI bills have been reported, including a Microsoft employee spreadsheet in August 2026. That is an adjacent fact. It is not a published sabotage case. The $28,000 figure is one voluntary entry, not an audited invoice.

Tokenmaxxing is the non-attack form: spending an allowance the account already pays for, before the period ends. The spreadsheet describes a dashboard variant of that form. Neither is TRCA.

## Reporting checked 2 October 2026

Published matches with an outlet and a date. Lab papers and vendor scans are labeled as such.

### Stolen key — new, and usable

| Source | What it shows | Limit |
|---|---|---|
| METR, 31 Aug 2026, [Update on Security at METR](https://metr.org/blog/2026-08-31-security-update/). The Hacker News, 1 Sep 2026, and The Register, 1 Sep 2026, are the same disclosure. | March 2026. A publicly exposed agent was prompted for its model-provider key. The key was then used for about three weeks. METR says the credits would have been worth about $600,000, and that the model developer had granted them free. No sensitive dataset was taken. | Free credits, not a collected invoice. |
| CloudSEK BeVigil, 7 Apr 2026 | 32 Google API keys hardcoded in 22 Android apps could call Gemini. Combined install claim is CloudSEK’s (over 500 million). They confirmed Gemini access, and file listings on one app (ELSA Speak). | Keys that could call the model. CloudSEK did not audit an invoice. Those apps are not treated as if they paid a bill. |
| The Hacker News, 9 Sep 2026, reporting Okta and Google. Cloud Security Alliance, 11 Sep 2026, is the same Okta dump. | One infostealer dump held 24 still-valid API keys for Gemini, OpenAI, Groq, and OpenRouter. A Mandiant case: an exposed GitHub token was used to turn on Gemini Enterprise and extra GPU capacity on the victim’s cloud. | Supply of keys, and cloud hijack for AI capacity. Not a new named inference invoice. |
| ZDNET, 29 Sep 2026, quoting John Hultquist / GTIG to the Financial Times | GTIG reports a major increase in LLMjacking during 2026, and resale of access to Anthropic, Google, and OpenAI. | Market color. No new victim bill. |

CloudSEK’s post also retells three reported bills ($15,400; a Japan conversion they put near $128,000; and the $82,314 already cited from Tom’s Hardware). Those are not new CloudSEK investigations. TechRadar, 11 April 2026, retells the $15,400 and the Japan figure and does not show they are CloudSEK’s own cases. No company is named. Those two figures are not cases on this page. The $82,314 stays the Tom’s Hardware line.

### Insider seat — still no hostile case

Bloomberg, 2 Jun 2026: Uber confirmed a $1,500 monthly token cap per employee per agentic coding tool (Claude Code, Cursor), after the year’s budget for those tools was gone in about four months. That is authorized use hitting a ceiling. It is a control. It is not sabotage.

The Microsoft spreadsheet is the same fact: voluntary entries, motive not shown.

### Runaway agent — pattern, not a new named bill

- Dark Reading / Forcepoint, September 2026, is the published pattern (tool chains, reasoning loops, growing chat). It is an explainer, not a Stolen key invoice.
- Zhou et al., arXiv 16 Jan 2026, *Beyond Max Tokens* (arXiv:2601.10955): a lab result. A normal-looking MCP tool can steer an agent into a long tool-call chain. Not a company invoice.
- Conf42, 24 Sep 2026, “the retry storm that ate my budget,” is a talk abstract ($400, unnamed). Not a case.
- OpenAI Developer Community, 20 Sep 2026. One security-scan request fanned out and spent a fresh weekly Codex allowance in about 44 minutes. The next worker could not start. First person. Not an attack. A weekly window is not several critical services sharing one month.
- Google AI Developers Forum, 30 Sep 2026. Agent runs burned the project tokens-per-minute cap. Request counts still looked fine, and the UI said the model was unlimited. Limits are per project, so another key in that project would not have helped. Not an attack. A per-minute cap is not a spent month.

### Agentic Service Degradation — the class is wider than an investigator

The class is any critical agentic service that gets disrupted, thinned, or cut in capacity because it shares an allowance. An investigator is the clearest case. It is not the only one. The 20 September and 30 September 2026 posts are Runaway agent stalls. They are not this class.

| Source | What it shows | Limit |
|---|---|---|
| Redress Compliance, Aug 2026 | Advisory claim: ServiceNow dev and sub-production draw the production Now Assist pool, and teams have exhausted that pool without a production user noticing. Median overage in their benchmark was 22% of tier spend. | Supports the ServiceNow example. Not a named outage. |

Still not found: a published attack in which someone spent a shared model token on purpose until a named critical service — investigator, fraud, or incident — could not start new work. Provider-wide capacity incidents (OpenAI, Anthropic) are the vendor running out of room. They are not this class.

Attackers already flood a human SOC with noise. Treating that same pressure as a way to spend an agentic SOC allowance is an extrapolation, not a published case.

## Extra effect: project-coupled blast radius

In the usual case the application stays up and the meter fails.

Several 2026 Google cases show a second ending: abuse detection **suspends the whole Cloud project**, so Maps, storage console, and customer data freeze with the Gemini bill. That is project-coupled blast radius. “Own key, own monthly limit” also means own project and own billing domain, for a public key versus the AI a critical service depends on.

## Timeline index

One line per event that belongs on the chronology and is not already a section in [trade-winds.md](trade-winds.md).

```timeline
2026-03-04 | case | Stolen key | Tom’s Hardware. $82,314 in 48 hours. | https://www.tomshardware.com/tech-industry/artificial-intelligence/gemini-api-key-thief-racks-up-usd82-314-in-charges-in-just-two-days-victim-facing-bankruptcy-affected-devs-call-for-basic-guardrails-against-catastrophic-usage-anomalies
2026-05-13 | case | Stolen key | Cybernews. About $67,000 in 19 hours. Colavo Ground. | https://cybernews.com/security/developers-go-bankrupt-over-legacy-google-cloud-api-keys/
2026-05-13 | case | Stolen key | The Register. $10,138 in minutes. A spend cap did not stop the live charge. | https://www.theregister.com/ai-ml/2026/05/13/google-users-fight-for-refunds-as-unauthorized-api-usage-bills-soar/5239160
2026-06-20 | case | Stolen key | CSA, LLMjacking Evolved. Stolen keys spent as the attacker’s compute. | https://labs.cloudsecurityalliance.org/research/csa-research-note-llmjacking-evolved-offensive-agentic-20260/
2026-08-26 | wind | none | The Next Web and TechRadar. A voluntary Microsoft spreadsheet. Not sabotage. | https://thenextweb.com/news/microsoft-employees-ai-spend-spreadsheet-europe-works-councils
2026-08-30 | case | Stolen key | BleepingComputer. Stolen Claude login sessions consumed paid usage. Not an API key. No dollar amount. | https://www.bleepingcomputer.com/news/artificial-intelligence/anthropic-warns-infostealer-malware-is-hijacking-claude-sessions-to-drain-usage/
2026-09-03 | case | Stolen key | FortiGuard Labs. A leaked AWS admin key invoked foundation models. Charges landed on the victim account. No dollar amount. | https://www.fortinet.com/blog/threat-research/someone-else-is-using-your-ai
2026-09-20 | stop | Runaway agent | OpenAI Developer Community. One security-scan request fanned out and spent a fresh weekly Codex allowance in about 44 minutes. The next worker could not start. | https://community.openai.com/t/fresh-weekly-codex-work-allowance-exhausted-in-44-minutes-by-security-scan-worker-fan-out/1399277
2026-09-21 | wind | Runaway agent | Dark Reading with Forcepoint. One request can still look normal and spawn endless work. | https://www.darkreading.com/application-security/how-ai-agents-can-trigger-runaway-costs
2026-09-25 | case | Stolen key | CARBONATO. Stolen LLM keys fund the attacker’s own agent. | https://securityaffairs.com/199716/malware/ai-powered-carbonato-botnet-steals-credentials-to-fund-its-own-llm-gateway.html
2026-09-30 | stop | Runaway agent | Google AI Developers Forum. A project tokens-per-minute cap, not a spent month. Not an attack. | https://discuss.ai.google.dev/t/the-real-cause-behind-ai-studio-build-quota-exceeded-the-agent-burns-your-projects-tpm-and-google-stays-silent/186027
```
