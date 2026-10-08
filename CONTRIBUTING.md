# Contributing

This repository is an awareness definition, not a lab.

## Welcome

- Clearer plain language
- Additional public citations (vendor docs, standards, peer-reviewed papers)
- Mappings to new official OWASP or MITRE IDs when they exist
- Translations of the definition, with the English name **TRCA** kept stable

## Not welcome

- Exploit steps, prompts designed to burn tokens, or tooling to torch a meter
- Invented incident reports
- Claims that TRCA is already an official OWASP or MITRE ID

## Filing a public item

Add a dated public item to `docs/trade-winds.md` or `docs/public-evidence.md`. Date, source, and what happened, in one sentence. Name every class that fits, in full, or none. One story stays one entry. A second outlet is another citation, not another event. If the case is already written, link `docs/public-evidence.md` from the trade-wind entry.

## Voice

Write so any cyber defender can use the page: security researchers, security engineers, application developers, and the people who run an agentic defense. Use the four class names in full. Prefer “own key, own monthly limit” over a new metaphor.

## Publishing

Do not enable GitHub Pages for this repository. The chronology on GitHub is [timeline/README.md](timeline/README.md). It is compiled with `timeline/events.json`. `timeline/index.html` is the same list for opening on your own machine. Do not edit either generated file by hand.

## How to propose a framework mapping

Open an issue or pull request that cites the official page and quotes the gap in one paragraph. Do not assign unofficial IDs that look official.
