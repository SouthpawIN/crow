# Crow — Deep Research & Analysis Specialist

![Crow](https://v3b.fal.media/files/b/0a9fe98b/hnTlB_PwDEGYcwbCCnuGk_iklnYDWu.png)

## What Crow Does
- **Investigates** topics deeply using web search and document extraction
- **Analyzes** markets, technologies, competitors, and trends
- **Synthesizes** findings into structured research reports
- **Cross-references** multiple sources to identify patterns and insights
- **Extracts** data from web pages, PDFs, and documentation

## Quick Start

### Install
```bash
hermes profile install https://github.com/SouthpawIN/crow
```

### Verify
```bash
hermes profile list
```

### Run
```bash
hermes chat --profile crow
```

## Example Prompts

- *"Research the current state of serverless databases — what are the best options?"*
- *"Find out how our competitors handle real-time data synchronization"*
- *"Search for academic papers on consensus algorithms and summarize the findings"*
- *"Investigate what happened to that startup we were watching last year"*
- *"Research the legal requirements for handling user data in the EU"*
- *"Compare the top 5 open-source queue systems and report on their tradeoffs"*
- *"Find technical documentation on implementing WebSockets at scale"*

## Key Features
- Multi-source intelligence — combines web search, document extraction, and API queries
- Pattern recognition — identifies trends and connections across sources
- Research transparency — explains where findings came from and confidence levels
- Output flexibility — produces everything from brief summaries to full research reports

## Integration with Other Agents
Crow is the fleet's research specialist. Senter dispatches research tasks to Crow. The findings are shared with Kashik (documentation), Chizul (implementation), and other agents. Anser defers to Crow when asked research questions.

## Configuration
`~/.hermes/profiles/crow/config.yaml`

Key settings:
- `search_engines` — preferred search sources (default: google, duckduckgo, brave)
- `research_timeout` — max time for research tasks in minutes (default: 30)
- `citation_style` — how to format sources (apa/mla/informal, default: informal)
- `output_length` — preferred report length (brief/standard/comprehensive, default: standard)

## Troubleshooting

**Research taking too long:** Lower `research_timeout` for quicker results, or adjust `output_length` to `brief`. Deep research needs time.

**Poor source quality:** Add specific domains to `trusted_sources` config, or use `site:` search operator in prompts to target authoritative sites.
**Part of the multi-agent fleet by SouthpawIN**
