# OpenSEO

Plugin that connects agents to [OpenSEO](https://openseo.so) through OpenSEO's official remote [Model Context Protocol](https://modelcontextprotocol.io/) server, plus twelve skills that guide complete SEO workflows.

Research keywords, competitors, backlinks, rankings, site audits, and AI visibility.

## Install

1. Open **Cursor Settings → Plugins**.
2. Search for **OpenSEO**.
3. Click **Install**, then complete the OpenSEO sign-in prompt.

Or run `/add-plugin openseo` in chat. In Grok Bot (0.49 or newer), add **OpenSEO** from the Marketplace.

To check the connection without using credits, ask: "Use OpenSEO to check my connection and list my projects."

## MCP

```json
{
  "mcpServers": {
    "openseo": {
      "type": "http",
      "url": "https://app.openseo.so/mcp"
    }
  }
}
```

Auth is OAuth 2.1 with PKCE and dynamic client registration. An unauthenticated request returns `401` with `resource_metadata` pointing at `https://app.openseo.so/.well-known/oauth-protected-resource/mcp`, and the authorization server is `https://app.openseo.so`. The client prompts for OpenSEO sign-in when the plugin connects. There is no client ID or API key to configure.

## Before you connect

You need an OpenSEO account. Hosted plans and usage credits are described at [openseo.so/pricing](https://openseo.so/pricing). Research tools use credits, and the server asks before larger paid batches. OpenSEO is open source and can also be [self-hosted](https://github.com/every-app/open-seo#self-hosting).

## What agents can do

| Category | Capabilities |
| --- | --- |
| Keywords | Research keywords, check metrics and SERPs, save and cluster terms |
| Competitors | Domain overviews, ranking keywords, content and keyword gaps |
| Backlinks | Backlink profiles and link prospects |
| Site audits | Crawl a site and prioritize fixes |
| Rankings | Track organic and Google Maps rankings |
| Google data | Search Console and Google Analytics for connected sites |
| AI visibility | Research AI prompts, track brand mentions, citations, and competitors |
| Reports | Save and share HTML reports |

The hosted runtime is the source of truth for tool names and schemas.

## Skills

AI prompt research, AI visibility audit, competitive landscape, competitor analysis, keyword clustering, keyword research, link prospecting, local SEO, SEO audit, SEO coach, SEO project setup, and SEO report. Start with **SEO coach** if you're not sure what to do next.

The skills are copied from [every-app/open-seo](https://github.com/every-app/open-seo/tree/main/plugins/openseo/skills), where OpenSEO maintains them.

## Docs

- OpenSEO: https://openseo.so
- MCP documentation: https://openseo.so/docs/mcp
- Server URL: https://app.openseo.so/mcp
- Privacy policy: https://openseo.so/privacy
- Terms: https://openseo.so/terms-and-conditions
- Support: support@openseo.so

Logo is OpenSEO's official mark.

## License

MIT
