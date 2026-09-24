# Awesome SEO MCP Servers [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Every Model Context Protocol server that connects an AI agent to SEO data. Search Console, keywords, backlinks, crawls, SERPs, and AI search visibility.

Every entry below was checked by hand in September 2026. We record who runs it, how you connect, what authentication it needs, and when it was last touched, because half the SEO MCP servers you find in a search are abandoned or have moved.

---

**Maintained by [RankSpot](https://www.rankspot.ai/)**, an AI search visibility platform that tracks brand mentions in ChatGPT, Claude, Gemini, and Google AI Overviews. RankSpot ships [its own MCP server](https://www.rankspot.ai/) and it is listed below in the same table as every competitor we could find, on the same terms. Spot a mistake in anyone's row? [Open a PR](CONTRIBUTING.md) and we will merge it.

---

## Contents

- [How to read this list](#how-to-read-this-list)
- [Official servers](#official-servers)
- [Google Search Console](#google-search-console)
- [Bing Webmaster Tools](#bing-webmaster-tools)
- [Keyword research and trends](#keyword-research-and-trends)
- [Backlinks and authority](#backlinks-and-authority)
- [SEO suites](#seo-suites)
- [SERP and web data](#serp-and-web-data)
- [Crawling and technical audits](#crawling-and-technical-audits)
- [Page speed and Core Web Vitals](#page-speed-and-core-web-vitals)
- [AI search visibility (GEO and AEO)](#ai-search-visibility-geo-and-aeo)
- [Indexing, sitemaps and llms.txt](#indexing-sitemaps-and-llmstxt)
- [Marketplace and app store SEO](#marketplace-and-app-store-seo)
- [Archived or superseded](#archived-or-superseded)
- [Connecting a server to your client](#connecting-a-server-to-your-client)
- [Gaps worth filling](#gaps-worth-filling)
- [Related lists](#related-lists)
- [Contributing](#contributing)

## How to read this list

| Column | Meaning |
| --- | --- |
| **Type** | `Remote` means a hosted URL you point your client at, nothing to install. `Local` means it runs on your machine, usually via npx or uvx. |
| **Auth** | What you need to connect. `OAuth` opens a browser login. `API key` needs a key from the vendor. `None` works out of the box. |
| **Stars** | GitHub stars, refreshed weekly by a workflow in this repo. Vendor servers with no public repo show `n/a`. |
| **Updated** | Last push to the default branch. Anything older than a year is worth testing before you rely on it. |

Servers marked **Official** are built and run by the company whose data they expose. Everything else is community built, which is not a knock, some community servers are better maintained than the official ones.

## Official servers

Run by the vendor. These are the ones to reach for first if you already pay for the underlying tool.

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [Ahrefs](https://docs.ahrefs.com/docs/mcp/) | Backlinks, keyword difficulty, competitor organic keywords, traffic history | Remote | OAuth | n/a | live |
| [Semrush](https://developer.semrush.com/api/v4/introduction/semrush-mcp/) | Core SEO data, Trends market intelligence, read-only Projects data | Remote | OAuth | n/a | live |
| [SE Ranking](https://seranking.com/api/integrations/mcp/) | 180+ tools covering keywords, backlinks, rank tracking, site audits, AI visibility | Remote | API key | n/a | live |
| [DataForSEO](https://github.com/dataforseo/mcp-server-typescript) | Raw SERP, keyword, backlink, on-page and domain analytics data across 12 API groups | Local | API key | 246 | 2026-09-01 |
| [SerpApi](https://github.com/serpapi/serpapi-mcp) | Live results from Google, Bing, Baidu, YouTube and other engines | Local | API key | 171 | 2026-09-21 |
| [Screaming Frog](https://www.screamingfrog.co.uk/blog/seo-spider-24/) | Native MCP in SEO Spider 24.0+, run and query crawls in natural language | Local | Paid licence | n/a | v24.0+ |
| [Local Falcon](https://github.com/local-falcon/mcp) | Geo-grid local rank tracking, Google Business Profile, competitor analysis | Remote | API key | 24 | 2026-09-21 |
| [SEOmonitor](https://github.com/BuntStudio/seomonitor-mcp-server) | Rank tracking, AI Overview visibility, keyword research, traffic forecasts | Remote | API key | 0 | 2026-09-14 |
| [Peec AI](https://docs.peec.ai/mcp/introduction) | Brand visibility, sentiment and citations across ChatGPT and Perplexity | Remote | API key | n/a | live |
| [RankSpot](https://www.rankspot.ai/) | AI visibility across ChatGPT, Claude, Gemini and AI Overviews, plus weekly action lists | Remote | OAuth | n/a | live |
| [Screpy](https://screpy.com/feature/seo-mcp/) | Project-scoped crawl, page, link, rank tracking, stored AI visibility, web vitals and uptime data | Remote | OAuth | n/a | live |
| [Google Analytics](https://github.com/googleanalytics/google-analytics-mcp) | GA4 reporting with schema discovery | Local | Google OAuth | 3260 | 2026-08-07 |
| [Google Ads](https://github.com/googleads/google-ads-mcp) | Read-only GAQL queries against Google Ads | Local | Google OAuth | 969 | 2026-09-21 |
| [Firecrawl](https://github.com/firecrawl/firecrawl-mcp-server) | Scraping and search, widely used for content and competitor research | Local | API key | 7497 | 2026-09-21 |
| [Apify](https://github.com/apify/apify-mcp-server) | Thousands of prebuilt scrapers including SERP, maps and marketplace crawlers | Remote | API key | 7908 | 2026-09-21 |
| [Bright Data](https://github.com/brightdata/brightdata-mcp) | Web access at scale, SERP scraping without getting blocked | Local | API key | 2655 | 2026-09-17 |
| [Oxylabs](https://github.com/oxylabs/oxylabs-mcp) | SERP and web scraping through the Oxylabs proxy network | Local | API key | 106 | 2026-09-07 |

**Endpoints for the remote ones**, so you do not have to dig through docs:

| Vendor | Endpoint |
| --- | --- |
| Ahrefs | `https://api.ahrefs.com/mcp/mcp` |
| Semrush | `https://mcp.semrush.com/claude/v1/mcp` |
| SE Ranking | `https://api.seranking.com/mcp` |
| Local Falcon | `https://mcp.localfalcon.com` |
| Peec AI | `https://api.peec.ai/mcp` |
| SEOmonitor | `https://mcp.seomonitor.com` |
| RankSpot | `https://mcp.rankspot.ai` |
| Screpy | `https://mcp.screpy.com` |

## Google Search Console

Google has no official GSC MCP server as of September 2026, so this category is entirely community built. `mcp-gsc` is the de facto standard.

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [AminForou/mcp-gsc](https://github.com/AminForou/mcp-gsc) | 19+ tools with regex filtering, the most used GSC server by a wide margin | Local | Google OAuth | 1610 | 2026-09-15 |
| [ahonn/mcp-server-gsc](https://github.com/ahonn/mcp-server-gsc) | Clean GSC wrapper, handles up to 25,000 rows per query | Local | Google OAuth | 273 | 2026-09-04 |
| [surendranb/google-search-console-mcp](https://github.com/surendranb/google-search-console-mcp) | GSC across Claude, Cursor, Windsurf and other clients | Local | Google OAuth | 38 | 2026-09-20 |
| [Magdoub/awesome-gsc-mcp](https://github.com/Magdoub/awesome-gsc-mcp) | 27 tools with a caching layer and rate limiting | Local | Google OAuth | 14 | 2026-02-25 |
| [serpfire/gsc-mcp-server](https://github.com/serpfire/gsc-mcp-server) | GSC plus built-in keyword cannibalisation detection | Local | Google OAuth | 11 | 2026-03-04 |

## Bing Webmaster Tools

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [isiahw1/mcp-server-bing-webmaster](https://github.com/isiahw1/mcp-server-bing-webmaster) | Bing Webmaster API endpoints for SEO management and analytics | Local | API key | 25 | 2026-02-10 |
| [zizzfizzix/mcp-server-bwt](https://github.com/zizzfizzix/mcp-server-bwt) | Exposes the full Bing Webmaster Tools API surface | Local | API key | 7 | 2025-04-11 |
| [urdigitalau/mcp-integrations](https://github.com/urdigitalau/mcp-integrations) | Bing Webmaster, WordPress and Microsoft Clarity in one repo | Local | API key | 0 | 2026-09-17 |
| [abhay-ramesh/mcp-bing-webmaster](https://github.com/abhay-ramesh/mcp-bing-webmaster) | Bing Webmaster API access for Claude and other clients | Local | API key | 0 | 2026-03-12 |

## Keyword research and trends

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [andrewlwn77/google-trends-mcp](https://github.com/andrewlwn77/google-trends-mcp) | Google Trends interest over time and related queries | Local | None | 28 | 2025-07-13 |
| [hithereiamaliff/mcp-keywords-everywhere](https://github.com/hithereiamaliff/mcp-keywords-everywhere) | Keywords Everywhere API for volume and related terms | Local | API key | 10 | 2026-04-02 |
| [mkotsollaris/kwrds-ai-mcp](https://github.com/mkotsollaris/kwrds-ai-mcp) | kwrds.ai keyword research and People Also Ask data | Local | API key | 7 | 2026-02-07 |
| [HasData/google-trends-mcp](https://github.com/HasData/google-trends-mcp) | Trends by region, interest over time, related queries | Local | API key | 5 | 2026-09-14 |
| [Amaculus/keywordinsights-mcp](https://github.com/Amaculus/keywordinsights-mcp) | Keyword Insights clustering and intent data | Local | API key | 3 | 2026-01-23 |

## Backlinks and authority

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [cnych/seo-mcp](https://github.com/cnych/seo-mcp) | Free Ahrefs-sourced backlinks and keyword ideas, no Ahrefs seat needed | Local | None | 260 | 2025-04-14 |
| [egebese/dataseo-mcp](https://github.com/egebese/dataseo-mcp) | Backlinks, keyword research and traffic estimation from Ahrefs data | Local | None | 192 | 2026-07-06 |
| [mrgoonie/seo-insights-mcp-server](https://github.com/mrgoonie/seo-insights-mcp-server) | Backlinks, keyword difficulty and traffic, with CLI support | Local | API key | 28 | 2025-11-24 |
| [metehan777/moz-mcp](https://github.com/metehan777/moz-mcp) | Moz API v3, Domain Authority and Page Authority. Moz has no official server | Local | API key | 15 | 2025-06-13 |
| [Rankparse/rankparse-mcp](https://github.com/Rankparse/rankparse-mcp) | 18+ tools for backlinks, domain authority and tech stack detection | Local | API key | 4 | 2026-05-23 |
| [MattiooFR/majestic-mcp](https://github.com/MattiooFR/majestic-mcp) | Majestic Trust Flow, Citation Flow and backlink data | Local | API key | 0 | 2026-02-03 |

## SEO suites

Multiple SEO functions behind one connection, mostly community wrappers around vendor APIs.

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [Skobyn/dataforseo-mcp-server](https://github.com/Skobyn/dataforseo-mcp-server) | Community DataForSEO server, 12 API categories and 40+ tools | Local | API key | 82 | 2026-06-04 |
| [mrkooblu/semrush-mcp](https://github.com/mrkooblu/semrush-mcp) | 77 tools against the Semrush API, predates the official server | Local | API key | 39 | 2026-09-09 |
| [metehan777/semrush-mcp](https://github.com/metehan777/semrush-mcp) | Lighter alternative Semrush implementation | Local | API key | 16 | 2025-06-03 |
| [TeamDay-AI/se-ranking-mcp](https://github.com/TeamDay-AI/se-ranking-mcp) | SE Ranking fork adding per-request credentials, useful for agencies | Local | API key | 0 | 2026-04-20 |
| [Minh42/seomatic-mcp](https://github.com/Minh42/seomatic-mcp) | Search Console, keywords, backlinks and AI visibility with approval-gated actions | Remote | API key | 0 | 2026-09-11 |
| [ezbiz-services/mcp-seo-marketing](https://github.com/ezbiz-services/mcp-seo-marketing) | Keyword research, SERP analysis, backlink checking, content optimisation | Local | API key | 0 | 2026-02-28 |

## SERP and web data

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [marcopesani/mcp-server-serper](https://github.com/marcopesani/mcp-server-serper) | Serper API search plus webpage scraping | Local | API key | 169 | 2025-03-13 |

See also SerpApi, Bright Data, Oxylabs and Apify in [Official servers](#official-servers).

## Crawling and technical audits

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [bzsasson/screaming-frog-mcp](https://github.com/bzsasson/screaming-frog-mcp) | Headless Screaming Frog runs with a locked-down tool surface, good for CI | Local | Paid licence | 88 | 2026-08-31 |
| [houtini-ai/seo-audit](https://github.com/houtini-ai/seo-audit) | Merges a first-party crawl with GSC, DataForSEO and Majestic into one audit | Local | API key | 20 | 2026-08-19 |
| [cmg8431/web-meta-scraper](https://github.com/cmg8431/web-meta-scraper) | Extracts Open Graph, JSON-LD and media metadata with SEO validation | Local | None | 10 | 2026-02-23 |
| [mgsrevolver/seo-inspector-mcp](https://github.com/mgsrevolver/seo-inspector-mcp) | Scans a project for common on-page SEO issues without leaving the editor | Local | None | 7 | 2025-03-07 |
| [Docker-Hunterpedia/seo-mcp-server](https://github.com/Docker-Hunterpedia/seo-mcp-server) | General SEO validation and analysis, ships as a Docker image | Local | None | 0 | 2026-02-14 |

## Page speed and Core Web Vitals

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [danielsogl/lighthouse-mcp-server](https://github.com/danielsogl/lighthouse-mcp-server) | 13+ tools for performance, accessibility, SEO and security audits | Local | None | 71 | 2026-09-21 |
| [PhialsBasement/Pagespeed-MCP-Server](https://github.com/PhialsBasement/Pagespeed-MCP-Server) | PageSpeed Insights data as MCP tools | Local | API key | 13 | 2025-09-13 |

## AI search visibility (GEO and AEO)

The newest and fastest moving category. Most entries here are under a year old.

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [RankSpot](https://www.rankspot.ai/) | Visibility across ChatGPT, Claude, Gemini and AI Overviews, plus weekly actions | Remote | OAuth | n/a | live |
| [Peec AI](https://docs.peec.ai/mcp/introduction) | Brand visibility, sentiment and citations, official server | Remote | API key | n/a | live |
| [thein-art/mcp-server-peecai](https://github.com/thein-art/mcp-server-peecai) | Community Peec.ai server with 38 tools and full CRUD | Local | API key | 2 | 2026-06-22 |
| [bestaiinsider/ai-visibility-mcp](https://github.com/bestaiinsider/ai-visibility-mcp) | Audits robots.txt per bot, JSON-LD, llms.txt and brand mentions in answers | Local | API key | 1 | 2026-05-23 |
| [maxaeo/maxaeo-ai-visibility-mcp](https://github.com/maxaeo/maxaeo-ai-visibility-mcp) | Local-first GEO and AEO audit covering llms.txt, schema and crawler readiness | Local | None | 1 | 2026-08-26 |
| [migkast/seoforgpt-mcp](https://github.com/migkast/seoforgpt-mcp) | Brand visibility in AI answers, competitor monitoring and cited sources | Local | API key | 1 | 2026-08-31 |
| [Instilla-AI/seontology-mcp-server](https://github.com/Instilla-AI/seontology-mcp-server) | Semantic SEO analysis using the SEOntology vocabulary | Local | None | 0 | 2025-09-04 |

## Indexing, sitemaps and llms.txt

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [janwilmake/LLMTEXT-mcp](https://github.com/janwilmake/LLMTEXT-mcp) | Converts llms.txt files into MCP servers, plus llms.txt tooling | Local | None | 51 | 2026-07-07 |
| [mugoosse/sitemap-mcp-server](https://github.com/mugoosse/sitemap-mcp-server) | Fetches, parses and crawls sitemaps for any site | Local | None | 7 | 2026-08-08 |
| [sharozdawa/indexnow-mcp](https://github.com/sharozdawa/indexnow-mcp) | Submits URLs via IndexNow and the Google Indexing API | Local | API key | 2 | 2026-03-22 |
| [cyber-kani/indexnow-mcp](https://github.com/cyber-kani/indexnow-mcp) | IndexNow submissions to Bing, Yandex, Seznam and Naver | Local | API key | 0 | 2026-07-07 |

## Marketplace and app store SEO

| Server | What it does | Type | Auth | Stars | Updated |
| --- | --- | --- | --- | --- | --- |
| [semihbugrasezer/seerxo](https://github.com/semihbugrasezer/seerxo) | Etsy listing optimisation, generates titles, descriptions and tags | Local | API key | 27 | 2026-09-15 |
| [KenanAtmaca/aso-mcp](https://github.com/KenanAtmaca/aso-mcp) | App Store Optimization keyword research and review sentiment, no API key | Local | None | 5 | 2026-06-12 |

## Archived or superseded

Listed so you stop finding them in search results and wondering why they do not work.

| Server | Status | Use instead |
| --- | --- | --- |
| [ahrefs/ahrefs-mcp-server](https://github.com/ahrefs/ahrefs-mcp-server) | Archived February 2026 | The [official remote server](https://docs.ahrefs.com/docs/mcp/) at `https://api.ahrefs.com/mcp/mcp` |
| [houtini-ai/seo-crawler-mcp](https://github.com/houtini-ai/seo-crawler-mcp) | Archived, merged into a larger tool | [houtini-ai/seo-audit](https://github.com/houtini-ai/seo-audit) |

Two more renames worth knowing, because older lists still point at the dead URLs: `egebese/seo-research-mcp` is now [egebese/dataseo-mcp](https://github.com/egebese/dataseo-mcp), and `semihbugrasezer/etsy-seo-mcp` is now [semihbugrasezer/seerxo](https://github.com/semihbugrasezer/seerxo).

## Connecting a server to your client

**Claude Code, remote server:**

```bash
claude mcp add --transport http ahrefs https://api.ahrefs.com/mcp/mcp
```

**Claude Code, local server:**

```bash
claude mcp add gsc -- uvx mcp-gsc
```

**Claude Desktop, Cursor, Windsurf and most other clients** use a JSON config file. Remote servers look like this:

```json
{
  "mcpServers": {
    "semrush": {
      "type": "http",
      "url": "https://mcp.semrush.com/claude/v1/mcp"
    }
  }
}
```

Local servers look like this:

```json
{
  "mcpServers": {
    "dataforseo": {
      "command": "npx",
      "args": ["-y", "dataforseo-mcp-server"],
      "env": {
        "DATAFORSEO_USERNAME": "your-username",
        "DATAFORSEO_PASSWORD": "your-password"
      }
    }
  }
}
```

Remote servers using OAuth will open a browser window the first time you connect, then reuse the credentials. Check each repo's README for the exact package name and required environment variables, since they vary.

## Gaps worth filling

Things people keep asking for that nobody has built well yet. Build one and we will list it.

- **Google Search Console, officially.** The most important free data source in SEO still has no first-party server.
- **Log file analysis.** Nothing exposes server logs so an agent can see which bots crawled what.
- **Internal linking.** No server maps internal link graphs or suggests link opportunities at scale.
- **Structured data validation.** Plenty of generators, no server that validates JSON-LD against Google's rich result requirements.
- **Hreflang and international SEO.** Completely unserved.
- **Moz, officially.** Only a community server exists, last updated mid 2025.
- **Content publishing.** WordPress has partial coverage, but nothing CMS-agnostic that handles Webflow, Ghost, Shopify and Framer.

## Related lists

- [awesome-seo-agent-skills](https://github.com/RankSpotAI/awesome-seo-agent-skills), Agent Skills that teach Claude Code, Codex and Cursor how to do SEO work. Most of them pull their data from a server on this list. Also maintained by us.
- [awesome-geo-tools](https://github.com/RankSpotAI/awesome-geo-tools), GEO and AI visibility platforms compared on engines tracked, refresh rate, price and data access. Also maintained by us.
- [sharozdawa/awesome-seo-mcp-servers](https://github.com/sharozdawa/awesome-seo-mcp-servers), a broader list covering MCP servers, agent skills and standalone tools. Useful prior art, and a source we cross-checked against while building this one.
- [josezuma/awesome-ai-visibility](https://github.com/josezuma/awesome-ai-visibility), GEO and AEO resources, AI crawler datasets and tools.
- [wong2/awesome-mcp-servers](https://github.com/wong2/awesome-mcp-servers), general purpose MCP directory across all categories.
- [Official MCP Registry](https://github.com/modelcontextprotocol/registry), the canonical index maintained by the protocol authors.

## Contributing

Additions and corrections are welcome, including corrections to entries for tools that compete with RankSpot. See [CONTRIBUTING.md](CONTRIBUTING.md) for what an entry needs.

The short version: the server has to actually exist, actually run, and speak MCP. We do not list roadmap announcements, and we do not list plain REST APIs with no MCP interface. Agent Skills go in [awesome-seo-agent-skills](https://github.com/RankSpotAI/awesome-seo-agent-skills) instead.

## License

[CC0](LICENSE). No rights reserved, copy it freely.

---

Maintained by [RankSpot](https://www.rankspot.ai/). If you want to know whether ChatGPT, Claude and Gemini recommend your brand, that is the problem we work on.
