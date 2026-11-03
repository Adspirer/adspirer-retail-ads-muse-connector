# Adspirer Retail Media Ads for Muse

Retail media agent for Amazon Ads and Walmart Connect. Review Sponsored Products, Sponsored Brands and Sponsored Display performance, track ACoS and ROAS, mine search terms, find wasted spend, and plan, create and optimize campaigns, with your approval before any change that affects spend.

This is Adspirer's company-owned **submission kit for the Muse hosted MCP connector** covering Amazon Ads and Walmart Connect. It is not a Muse plugin runtime. The hosted Adspirer service is the runtime; this repository holds review materials only. The main connector, covering every platform, has its own kit at [Adspirer/adspirer-muse-connector](https://github.com/Adspirer/adspirer-muse-connector).

## Connection

| Field | Value |
| --- | --- |
| Connection type | Existing MCP |
| Endpoint | `https://mcp.adspirer.com/retail-ads` |
| Transport | Streamable HTTP |
| Authentication | OAuth with PKCE (S256) |
| Registration | Dynamic client registration |
| Support | support@adspirer.com |

## Connector overview (guidelines §5.1)

- Who it's for: Amazon sellers and vendors, Walmart Marketplace sellers and suppliers, and the agencies that run their ads.
- What it does: ACoS, ROAS and spend reporting, search-term mining, keyword and negative-keyword management, bid and budget changes, out-of-budget alerts, and paused campaign creation for Amazon Sponsored Products, Sponsored Brands and Sponsored Display and Walmart Connect Sponsored Products.
- Why it beats the browser: it reads the user's own advertiser accounts through the Amazon Ads API and Walmart Connect API, so answers come from real account data, and it finishes approved changes in the account instead of sending the user to the advertising console.

An Adspirer account, an applicable Adspirer plan, and authorized access to at least one Amazon Ads profile or Walmart Connect advertiser. Walmart Connect is available for US advertisers. Capabilities depend on platform permissions, eligibility, plan limits and the platforms' API limits. Advertising spend is billed separately by Amazon and Walmart. Muse connector availability is subject to review and enablement.

## Tools

8 top-level tools, each classified Read, Write or Sensitive write in [submission/TOOLS.md](submission/TOOLS.md). Every platform has a read-only router that the server enforces, and every write router asks for confirmation on the server before it runs.

## Submission workflow

1. Review `submission/connector.json`, `submission/FORM.md` and `submission/TOOLS.md`. The JSON is our internal source of truth, **not a published Muse manifest format**.
2. Run `python3 scripts/package.py --check` and `python3 scripts/package.py`.
3. Complete the [reviewer checklist](submission/REVIEWER.md) and arrange reviewer access privately.
4. Use the [Muse submission portal](https://muse.ai/platform). Copy the form details, upload the Adspirer icon, and attach or link the tool documentation.
5. Record the receipt and review state in a submission-tracking issue. Never put credentials or private reviewer details in public issues.

CI validates and builds a reviewer ZIP on pushes, pull requests and manual runs. It never submits to Muse.

## Status

Kit prepared 2026-11-02. Not yet submitted. Muse authorization and live tool execution remain to be verified in Muse.

## Documentation

- [Muse setup](https://www.adspirer.com/docs/ai-clients/muse)
- [MCP documentation](https://www.adspirer.com/docs/mcp)
- [Tool catalog](https://www.adspirer.com/docs/agent-skills/tools)
- [Security and data handling](https://www.adspirer.com/docs/knowledge-base/security)
- [Privacy policy](https://www.adspirer.com/privacy)
