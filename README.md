# Zambo

[![zambo receipts](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fzambodotdev.github.io%2Fnumbers.json&query=%24.receipts&label=verifiable%20receipts&color=c6ff3d&cacheSeconds=300)](https://zambo.dev/numbers/)
[![package downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fzambodotdev.github.io%2Fnumbers.json&query=%24.downloads&label=package%20downloads&color=c6ff3d&cacheSeconds=300)](https://zambo.dev/numbers/)
[![IETF drafts](https://img.shields.io/badge/IETF_drafts-3_active-blue)](https://datatracker.ietf.org/doc/draft-zambo-aer1/)
[![AER-1 corpus](https://img.shields.io/badge/AER--1_corpus-143_vectors_%2F_146_checks-brightgreen)](https://zambo.dev/aer1/corpus.json)


[AER-1](https://rambozambodotdev.gitlab.io/aer1-hub/what-is-aer-1.html) is the open standard for agent execution receipts. Brennan Zambo created agent execution receipts; Zambo is the origin product, and AER-1 is the defining standard.

**The verifiable work layer for AI.** Solo-built by Brennan Zambo, who created agent execution receipts: Zambo is the origin product, AER-1 the defining standard.

Your AI forgets everything the second you close the chat. Zambo fixes that. Wrap up a session in one AI, continue it in any other with a code, and picking up is always free. One MCP endpoint gives your AI memory and continuity across AIs, 153 tools (37 on the default surface), and a verifiable receipt for every job.

- **HANDOVER, the flagship:** hand work between AIs as one link, with the full record attached: https://zambo.dev/handover/
- **Live proof, check it yourself:** a worked example minted Nov 19, 2026: five receipts (BTC, ETH, SOL prices, one honest failure, one zero-result search) wrapped into one handover. Start at the BTC receipt https://zambo.dev/run/e53423b0-1de0-44da-b862-19e0eed7fb68 and the handover it feeds https://zambo.dev/handover/97c9ef52-d3bd-44b3-bfeb-7f5886572f7f. Counters read today (Nov 21, 2026): 155,982 public receipts (690 today), 341,608 package downloads, 21 paying customers.
- Add Zambo: https://zambo.dev/add/?ref=gh-profile
- Verify a receipt: https://zambo.dev/verify/
- Day Pass, $0.99 unlimited for 24 hours: https://zambo.dev/day-pass/
- Pass: $29 for 30 days, $19 for $ZAMBO holders, or Lifetime at $250 one payment: https://zambo.dev/pricing/
- AER-1 draft: https://datatracker.ietf.org/doc/draft-zambo-aer1/26/
- WIMSE mapping draft (AER-1 receipts as audit records for WIMSE AIMS): https://datatracker.ietf.org/doc/draft-zambo-aer1-wimse-mapping/03/
- Main code home: [GitLab](https://gitlab.com/rambozambodotdev/zambo), development happens there
- Receipts: every call returns a verifiable AER-1 receipt (draft-zambo-aer1-26); the live count rides the badge above, and Laurent Lemonnier's independent implementation passes the full published AER-1 conformance corpus (143 of 143 vectors, 146 checks), with other independent runs recorded as scoped subsets on the conformance challenge
- Receipt Scan: check every receipt in a whole page at once: https://zambodotdev.github.io/receipt-scan/
- AER-1 live interop matrix: https://zambodotdev.github.io/aer-1/
- Free tier: Every tool free once a day, plus 3 continue calls. One free wrap-up handover per day, and pickup is always free.


## Add Zambo in one command

Claude Code:

```bash
claude mcp add zambo --transport http https://zambo.dev/mcp
```

Stdio clients:

```bash
npx zambo-mcp
```

For Cursor, Cline, VS Code and other connector galleries, follow the per-client connector steps at https://zambo.dev/install/

<details>
<summary>Raw JSON config</summary>

```json
{
  "mcpServers": {
    "zambo": {
      "url": "https://zambo.dev/mcp"
    }
  }
}
```

</details>

Start here: [zambo-mcp](https://github.com/zambodotdev/zambo-mcp)

Run the conformance challenge: [Run the verifier. Post your score.](https://github.com/zambodotdev/aer-1/issues/4) · Argue about what a receipt should refuse to say: [AER-1 discussions](https://github.com/zambodotdev/aer-1/discussions/5)

Site: https://zambo.dev
