# Verdict — MCP server (hosted)

**Send anything. Get the truth.**

Verdict checks anything suspicious — a text, an email, a marketplace
listing, a job offer, an investment pitch, a link — and returns a plain
verdict: **REAL**, **SUSPICIOUS**, or **LIKELY SCAM**, with every check
shown in plain words and a clear "what to do next." Behind the verdict:
links are followed safely on the server (private and internal addresses
are refused before any fetch), look-alike and punycode domains are caught,
domain age is read from the registry (RDAP), sender rules are checked
(SPF/DMARC), known-bad lists are consulted, and the words themselves are
scored for the pressure and payment tricks scams run on. Every check
returns a **signed verdict certificate** and a shareable link that never
contains the pasted content. Content is processed, not stored.

This repository is the **public listing** for the hosted Verdict MCP
server: documentation and manifests only, no server source. The service
is operated by **2351485 ALBERTA INC.** Support: **info@aimlds.org**.

## Connect

- **Endpoint:** `POST https://verdict.aimlds.org/mcp` (streamable HTTP, stateless)
- **Auth:** none — the free tier is keyless (3 checks/day per network)
- **Web:** https://verdict.aimlds.org (paste anything, same verdict)
- **Email:** forward any suspicious email to `check@aimlds.org` and get the verdict back by reply
- **Health:** https://verdict.aimlds.org/health

## Client config

Any MCP client that supports remote streamable-HTTP servers (Cline included):

```json
{
  "mcpServers": {
    "verdict": {
      "url": "https://verdict.aimlds.org/mcp"
    }
  }
}
```

## Tools (2)

| Tool | What it does |
|---|---|
| `check_message` | Check any suspicious text — a message, email, listing, job offer, investment pitch or link — and get the verdict, every check, a warning score, what to do next, a signed verdict certificate, and a shareable verdict link |
| `check_url` | Check a single URL: it is followed safely server-side, its domain age and sender rules are read, and look-alike / known-bad checks run against it |

## Tiers (Stripe — live on the product site)

| Tier | Price | Checks | For |
|---|---|---|---|
| Free | — | 3/day | trying it, the odd suspicious message |
| Pro | $6 USD/mo | unlimited | one person — plus threat-intel checks and the signed verdict certificate on every check |
| Family | $12 USD/mo | unlimited | 5 people on one family code, with a summary-only guard page that shows the payer every likely scam the household runs into |

Verdicts say "likely," never a guarantee — the checks and their evidence
are always shown so a person can judge for themselves.

## Links

- Product: https://verdict.aimlds.org
- Privacy: https://verdict.aimlds.org/privacy
- Terms: https://verdict.aimlds.org/terms
- Releases: https://verdict.aimlds.org/releases

Conceived by [Nrupal Akolkar](https://nrupalakolkar.com) · Built by
[Muse](https://muse.ai/join) — join Muse, then redeem code **101EEK** in
Settings within 48 hours of joining and we both earn tokens.
