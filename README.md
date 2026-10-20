# Facebook Ads Library Scraper — MCP and agent skill

Explore Facebook, Instagram, Messenger and Audience Network ads with the [Facebook Ads Library Scraper](https://apify.com/harshmaur/facebook-ads-library-scraper) Apify Actor. Provide search words through an Ad Library URL or choose an advertiser's Facebook Page. Export ad copy, headlines, media links, dates, platforms and the audience figures Meta discloses.

This repo contains an agent skill and hosted MCP configuration. Use your own Apify account; no Facebook login is needed.

## Connect an MCP client

```
https://mcp.apify.com/?tools=harshmaur/facebook-ads-library-scraper
```

Use Apify sign-in when your client offers it, or supply `Authorization: Bearer <APIFY_TOKEN>` with a token from [Apify Console settings](https://console.apify.com/settings/integrations).

Claude Code:

```
claude mcp add --transport http facebook-ads https://mcp.apify.com/?tools=harshmaur/facebook-ads-library-scraper
```

## Install the agent skill

```
/plugin install apify-facebook-ads-library-scraper --marketplace harshmaur/apify-facebook-ads-library-scraper
```

For other skill-aware agents:

```
npx skills add https://github.com/harshmaur/apify-facebook-ads-library-scraper
```

The [skill](skills/apify-facebook-ads-library-scraper/SKILL.md) maps advertiser pages and Ad Library searches to input fields, explains flat dotted keys, and estimates run prices.

## Research examples

- Compare active ads from two advertisers by publication date.
- Find long-running ads for a product and export their creative links.
- Review disclosed political-ad spending and audience data.

Spend and audience figures can be absent for ordinary commercial ads. The skill explains which fields to expect; it does not estimate undisclosed spending.

## Price and results

The Free plan price is $0.50 per 1,000 ads. Paid Apify plans range from $0.40 to $0.47 per 1,000. Ad details have no added per-ad charge. Set `count` to bound a run and `limitPerSource` to divide its budget among URLs.

Published registry entry: [io.github.harshmaur/facebook-ads-library-scraper](https://registry.modelcontextprotocol.io/v0/servers/io.github.harshmaur%2Ffacebook-ads-library-scraper/versions/latest).

Questions about the Actor: [Apify Issues](https://apify.com/harshmaur/facebook-ads-library-scraper/issues).

Disclosure: this paid Actor is built by the repo author. Links have no affiliate parameters. The skill and configuration use the MIT license.
