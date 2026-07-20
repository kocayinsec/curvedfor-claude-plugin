# CurvedFor Claude plugin

This plugin connects Claude to the public CurvedFor Launch Page Proof Pack MCP server and adds a bounded workflow skill.

The connector is read-only. It can return the public structure-utility contract, prepare a bounded brief, and run deterministic structural checks. It does not write tool inputs to CurvedFor application data or application logs, invoke a model, create a CurvedFor run or Receipt, access an account, create an order, start checkout, charge money, or initiate a review or SLA. The primary Vercel host retains plan-bounded request/function metadata and application log messages; connector code never logs tool payloads.

## Install for development

```bash
git clone https://github.com/kocayinsec/curvedfor-claude-plugin.git
cd curvedfor-claude-plugin
claude plugin validate . --strict
claude --plugin-dir .
```

Then inspect `/mcp` and invoke `/curvedfor:launch-page-proof-pack`.

The configured remote endpoint is the live no-auth first-party URL `https://mcp.curvedfor.com/mcp`, served by the isolated Vercel deployment.

## Example prompts

- “Show the exact six-section launch-page structure and everything the checker does not verify.”
- “Prepare a bounded brief from these notes and list the required inputs I have not supplied.”
- “Check this Markdown for section order, the 700-word ceiling, and exactly three headlines.”

## Policies and support

- Documentation: https://www.curvedfor.com/docs/mcp
- Privacy Policy: https://www.curvedfor.com/privacy
- Terms of Service: https://www.curvedfor.com/terms
- Support: https://www.curvedfor.com/contact

Do not submit credentials, payment-card data, private links, health data, government identifiers, or confidential client material to the connector.
