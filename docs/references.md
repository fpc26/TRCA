# References

Retrieved for this working set in September 2026. Primary documents first.

## Standards

- OWASP GenAI / LLM Top 10 2026. Unbounded Consumption is LLM06:2026. https://github.com/GenAI-Security-Project/GenAI-LLM-Top10
- Official publication page: https://genai.owasp.org/resource/owasp-genai-llm-top-10-2026/

## MITRE

- ATT&CK T1496 Resource Hijacking. https://attack.mitre.org/techniques/T1496
- ATT&CK T1496.004 Cloud Service Hijacking, under Resource Hijacking. Compromised SaaS, including LLMJacking. The page includes significant financial cost, used-up service quotas, and impact on availability. Created 25 Sep 2024. Last modified 15 Apr 2025. https://attack.mitre.org/techniques/T1496/004
- ATT&CK T1499 Endpoint Denial of Service. https://attack.mitre.org/techniques/T1499
- ATLAS AML.T0034 Cost Harvesting, and AML.T0034.000 Excessive Queries, AML.T0034.001 Resource-Intensive Queries, AML.T0034.002 Agentic Resource Consumption. Read on the techniques index, 6 Oct 2026. The .002 procedure is coerced expensive tool calls, including by prompt injection or tool-data poisoning. https://atlas.mitre.org/techniques

## Vendor meters

- Microsoft Learn, Security Compute Units and capacity. https://learn.microsoft.com/en-us/copilot/security/security-compute-units-capacity
- Microsoft Learn, Security Copilot inclusion for Microsoft 365 E5 and E7. https://learn.microsoft.com/en-us/copilot/security/security-copilot-inclusion
- Google SecOps, Agentic SOC Security Tokens. https://docs.cloud.google.com/chronicle/docs/agentic-soc/security-tokens
- Google Cloud, FinOps for SecOps. https://cloud.google.com/transform/finops-for-secops-how-to-optimize-the-agentic-soc-for-value
- CrowdStrike licensing FAQ, Charlotte AI credits. https://www.crowdstrike.com/en-us/legal/crowdstrike-licensing/
- CrowdStrike, Secure Agent Harness Execution (economic containment). https://www.crowdstrike.com/en-us/blog/secure-agent-harness-execution-preventing-escape/
- Elastic Security Labs, Agentic SOC token-budget architecture. https://www.elastic.co/security-labs/agentic-soc-token-budget-architecture
- Alibaba Cloud, Agentic SOC billing model upgrade. https://www.alibabacloud.com/help/en/security-center/notice-of-upgrade-to-the-agentic-soc-billing-model

## Trade winds

Each event is aligned to Insider seat, Stolen key, Runaway agent, Agentic Service Degradation, or none. Not a new case. The log is [trade-winds.md](trade-winds.md).

- Sumo Logic, January 2026, Token Torching. A prior name for the bill. https://www.sumologic.com/blog/token-torching-ai-attack
- Bitsight, July 2026, Token Torching. Same name, second outlet. https://www.bitsight.com/blog/what-is-token-torching-guide-to-new-cyber-threat
- Kaspersky, September 2026, Denial of Wallet as a cost flood against AI agents. https://www.kaspersky.com/blog/tokenomics-ai-cost-ddos/56455/
- Security Affairs, 21 September 2026, the target is the agent. Poisoned skills and injection. Not a meter. https://securityaffairs.com/199454/ai/the-target-is-no-longer-the-model-its-the-agent.html
- ZDNET, Charlie Osborne, 29 September 2026, the 2026 rise in LLMjacking. Market color, no new victim bill. https://www.zdnet.com/innovation/llmjacking-business-ai-bill-cost-how-to-stop
- Rob Wright, Dark Reading, 5 October 2026, “Need for Speed: AI-Driven Attacks Change Security Strategies.” AI-speed attacks, and AI defense in the SOC. No token or bill in the piece. https://www.darkreading.com/cyber-risk/ai-attacks-security-strategies
- The published investigator meters (Microsoft SCUs, Google Security Tokens, CrowdStrike credits, Elastic, Alibaba) are the product half of the same wind. Sources are under Vendor meters above. The table is in [agentic-soc.md](agentic-soc.md).

## Public reporting that supports Stolen key and Runaway agent

- Jai Vijayan, Dark Reading, 21 September 2026, “How AI Agents Can Trigger Runaway Costs for Enterprises” (Forcepoint five shapes: Denial of Wallet, agent tool fan-out, reasoning-loop exhaustion, context accumulation, model extraction). An explainer for Runaway agent. It does not cover abuse of a valid seat, and it is not a Stolen key invoice. https://www.darkreading.com/application-security/how-ai-agents-can-trigger-runaway-costs
- Cloud Security Alliance AI Safety Initiative, 20 June 2026, “LLMjacking Evolved: Stolen AI Compute as Offensive Infrastructure.” Stolen-key inference abuse in the wild; cost asymmetry on victim accounts; agentic use of stolen compute. Supports **02 Stolen key** and ATT&CK T1496.004. Does **not** describe an investigator quota. https://labs.cloudsecurityalliance.org/research/csa-research-note-llmjacking-evolved-offensive-agentic-20260/
- Aikido, 20 May 2026, a poisoned VS Code extension (Nx Console) on a developer machine. Tokens and secrets on disk needed rotation. Not an AI-bill invoice. https://www.aikido.dev/blog/vs-code-extension-github-breach
- Cybernews, 13 May 2026, legacy Maps/Firebase keys and bankruptcy-risk bills (incl. Colavo Ground). https://cybernews.com/security/developers-go-bankrupt-over-legacy-google-cloud-api-keys/
- The Register, 13 May 2026, unauthorized Gemini bills and Maps-key reuse. https://www.theregister.com/ai-ml/2026/05/13/google-users-fight-for-refunds-as-unauthorized-api-usage-bills-soar/5239160
- Truffle Security, 28 Jun 2026, unrestricted keys rejected for Gemini. https://trufflesecurity.com/blog/google-fixes-the-gemini-api-key-privilege-escalation-issue
- Truffle Security, 25 Feb 2026, the public write-up of that same finding. The page records a private report to Google on 21 Nov 2025. Google called it a bug on 2 Dec 2025. A blog-index date of 16 Dec 2025 is not the date on the page. “Thousands of dollars per day” is the lab’s ceiling, not a checked bill. https://trufflesecurity.com/blog/google-api-keys-werent-secrets-but-then-gemini-changed-the-rules
- ThreatDown / Security Affairs, 25 Sep 2026, CARBONATO steals LLM keys to fund its own gateway. https://securityaffairs.com/199716/malware/ai-powered-carbonato-botnet-steals-credentials-to-fund-its-own-llm-gateway.html
- BleepingComputer, 24 Sep 2026, same CARBONATO research, second outlet. https://www.bleepingcomputer.com/news/security/new-carbonato-malware-uses-ai-agents-to-hijack-exposed-docker-hosts/
- Dark Reading, Alexander Culafi, 28 Sep 2026, same CARBONATO research, second outlet. https://www.darkreading.com/identity-access-management-security/carbonato-botnet-ai-agent-hacked-docker-hosts
- Case table and honesty rules: [public-evidence.md](public-evidence.md)

## Prior names and adjacent reporting

Token Torching, the Kaspersky Denial-of-Wallet note, and the “target is the agent” piece are indexed in [trade-winds.md](trade-winds.md). They are not repeated here.

- Clawdrain: stealthy token exhaustion, arXiv:2603.00902. https://arxiv.org/abs/2603.00902
- Forcepoint, Unbounded Consumption / Denial of Wallet. https://www.forcepoint.com/blog/x-labs/unbounded-consumption
- TechRadar, 27 Aug 2026, reports a voluntary Microsoft spreadsheet with one $28,000 / 28-day AI figure. Headline is stronger than the body. Not a sabotage case. https://www.techradar.com/pro/microsoft-cracks-down-on-employee-ai-use-after-one-worker-spent-usd28-000-in-28-days
- The Next Web, 26 Aug 2026, same spreadsheet: median about $300, highest reported $28,000, roughly 350 voluntary entries. https://thenextweb.com/news/microsoft-employees-ai-spend-spreadsheet-europe-works-councils

## OSINT added 2 Oct 2026

- METR, 31 Aug 2026, stolen inference key via a prompted agent; about three weeks of credits, retail value about $600,000, granted free. Not an invoice. https://metr.org/blog/2026-08-31-security-update/
- CloudSEK, 7 Apr 2026, 32 hardcoded Google keys in 22 Android apps could call Gemini. Scan result, not an audited bill for those apps. https://www.cloudsek.com/blog/hardcoded-google-api-keys-in-top-android-apps-now-expose-gemini-ai
- The Hacker News, 9 Sep 2026, Okta stealer dump (24 live AI API keys) and a Mandiant case of a GitHub token used to stand up Gemini Enterprise on the victim’s cloud. https://thehackernews.com/2026/09/infostealer-logs-expose-replayable-ai.html
- Bloomberg, Natalie Lung, 2 Jun 2026, Uber’s $1,500 monthly cap per coding tool. Authorized spend, not an attack. https://www.bloomberg.com/news/articles/2026-06-02/uber-caps-usage-of-ai-tools-like-claude-code-to-cut-costs
- Zhou et al., 16 Jan 2026, Beyond Max Tokens, arXiv:2601.10955. Lab tool-chain amplification. Not a victim bill. https://arxiv.org/abs/2601.10955
- Sysdig, 7 Feb 2025, and Dark Reading the same day, DeepSeek keys inside a reverse proxy. Fifty-five keys is a count in one proxy. Dollar lines on the Sysdig page are estimates, not a named invoice. https://www.sysdig.com/blog/llmjacking-targets-deepseek https://www.darkreading.com/application-security/llm-hijackers-deepseek-api-keys
- Sysdig, 24 Feb 2026, restates the 2024 LLMjacking research and names Operation Bizarre Bazaar. No new victim. The $46,000-per-day line is the old estimate. https://www.sysdig.com/blog/llmjacking-from-emerging-threat-to-black-market-reality
- OpenAI Developer Community, 20 Sep 2026, one security-scan fan-out spent a fresh weekly Codex allowance in about 44 minutes and the next worker could not start. Not an attack. https://community.openai.com/t/fresh-weekly-codex-work-allowance-exhausted-in-44-minutes-by-security-scan-worker-fan-out/1399277
- Google AI Developers Forum, 30 Sep 2026, agent runs burned a shared project tokens-per-minute cap while request counters still looked fine. https://discuss.ai.google.dev/t/the-real-cause-behind-ai-studio-build-quota-exceeded-the-agent-burns-your-projects-tpm-and-google-stays-silent/186027
- Redress Compliance, 7 Aug 2026, Now Assist dev and sub-production draw the production pool. Advisory benchmark, not a named outage. https://redresscompliance.com/servicenow-now-assist-consumption-overage-2026


