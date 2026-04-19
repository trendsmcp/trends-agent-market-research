# trends-agent-market-research

Live consumer demand data for AI market research agents. One MCP
connection to Amazon, Google Shopping, TikTok, Reddit, App Store, news,
and more. Replace expensive panel data with live signals on a free tier.

> Live trend data for AI agents. One connection. Every platform.
> Powered by [trendsmcp.ai](https://trendsmcp.ai)

## Why this exists

Market research agents need signals on consumer demand, brand
perception, and category dynamics. Trends MCP gives your agent search
demand (Google, Google Shopping), purchase intent (Amazon), social
buzz (TikTok, Reddit), and news (volume and sentiment) through one MCP
server, with one API key and a normalized 0 to 100 scale.

## Get your free API key

1. Go to [trendsmcp.ai](https://trendsmcp.ai)
2. Enter your email, key sent instantly
3. 100 free requests per month, no credit card

[Get your free key](https://trendsmcp.ai)

## Connect any AI tool in 30 seconds

Pick the client your research workflow uses. Full snippets are at
[trendsmcp.ai/docs](https://trendsmcp.ai/docs).

- **Claude Desktop / Claude.ai / Claude mobile.** Add a custom
  connector with name `Trends MCP` and server URL
  `https://www.trendsmcp.ai/mcp`.
- **ChatGPT.** Add as a custom connector on a plan that supports them,
  or call the REST API from a Custom GPT Action.
- **Cursor / Windsurf / VS Code Copilot.** MCP config in the IDE for
  data plus notebook workflows.
- **Direct API from Python.** Drop into your existing analytics stack.

```python
import requests

res = requests.post(
    "https://api.trendsmcp.ai/api",
    headers={"Authorization": "Bearer YOUR_API_KEY"},
    json={"source": "amazon", "keyword": "air fryer"},
).json()
print(res)
```

## What you can ask a market research agent

- "Using TrendsMCP, show me 5 year Amazon search trend for `air fryer`."
- "Via TrendsMCP, compare Google Shopping growth for `running shoes` and `hiking boots` over 1 year."
- "Using TrendsMCP, find the fastest growing subreddits in personal finance over 6 months."
- "Via TrendsMCP, list Amazon Best Sellers Top Rated right now in `home and kitchen`."
- "Using TrendsMCP, get TikTok hashtag growth for `matcha` over 90 days."
- "Via TrendsMCP, what are the App Store Top Free apps right now?"
- "Using TrendsMCP, show me news sentiment for `Patagonia` over 6 months."

## Market research use cases this unlocks

- **Category sizing and demand mapping.** Compare Amazon, Google
  Shopping, and Google Search demand across products on one scale.
- **Brand health monitoring.** Track Google Search interest, news
  sentiment, and Reddit buzz for any brand over time.
- **Concept testing for new products.** Validate demand before
  launching, using TikTok hashtags and Amazon search history as proxies.
- **Whitespace discovery.** Find rising subreddits and TikTok hashtags
  in your category before competitors do.
- **Consumer trend reports.** Have an AI agent pull data, build the
  charts, and draft the report in one chat.
- **Replacement for slow survey loops.** Use real demand signals as a
  fast first pass before commissioning a panel study.

## Three tools your AI gets

- `get_trends`, historical time series for any keyword on any source
  (5 years weekly, 30 days daily where supported).
- `get_growth`, percentage change over any period (7D, 1M, 3M, 6M, 1Y,
  YTD, custom dates).
- `get_top_trends`, what is trending right now across live platform feeds.

## All data sources in one connection

One API key gives your market research agent every keyword source and
every live feed below.

### Keyword sources (Get Trends and Get Growth)

| source | What it measures | Keyword format |
| --- | --- | --- |
| `google search` | Google search volume | Any keyword or phrase |
| `google images` | Google image search volume | Any keyword or phrase |
| `google news` | Google News search volume | Any keyword or phrase |
| `google shopping` | Google Shopping search volume | Any keyword or phrase |
| `youtube` | YouTube search volume | Any keyword or phrase |
| `tiktok` | TikTok hashtag volume | Hashtag or topic |
| `reddit` | Subreddit subscribers | Subreddit name only, no `r/` prefix |
| `amazon` | Amazon product search volume | Product name or category |
| `wikipedia` | Wikipedia page views | Article title or topic |
| `news volume` | News article mention volume | Any keyword or phrase |
| `news sentiment` | News sentiment score (positive / negative) | Any keyword or phrase |
| `app downloads` | Mobile app download estimates (Android) | Package id or app identifier |
| `npm` | npm package weekly downloads | Exact package name e.g. react |
| `steam` | Steam concurrent players (monthly) | Game display name e.g. Elden Ring |

All values are normalized to a 0 to 100 scale where the pipeline supports
it, so you can compare different sources directly.

### Live leaderboards (Get Top Trends)

Google Trends, Google News Top News, TikTok Trending Hashtags, YouTube
Trending, X (Twitter) Trending, Reddit Hot Posts, Reddit World News,
Wikipedia Trending, Amazon Best Sellers Top Rated, Amazon Best Sellers by
Category, App Store Top Free, App Store Top Paid, Google Play, Top
Websites, Spotify Top Podcasts, Steam Most Played, GitHub Trending Repos,
IMDb MOVIEmeter, Trending Books.

The source list evolves over time. Authoritative reference at
[trendsmcp.ai/docs](https://trendsmcp.ai/docs).

## Pricing

Free forever for 100 requests per month. Paid plans available. See
[trendsmcp.ai/pricing](https://trendsmcp.ai/pricing).

## Resources

- [Get a free API key](https://trendsmcp.ai)
- [Documentation and full reference](https://trendsmcp.ai/docs)
- [Pricing](https://trendsmcp.ai/pricing)
- [All TrendsMCP repositories](https://github.com/trendsmcp)

## Security

Never commit your API key to a public repository. Use environment
variables or your OS secret store. Keys can be rotated at any time from
your TrendsMCP dashboard. The `YOUR_API_KEY` placeholder above is a
literal string to replace with your own key after you copy the snippet
locally.

## License

MIT. See [LICENSE](./LICENSE).
