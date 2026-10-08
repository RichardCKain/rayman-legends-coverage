# Rayman Legends: Retold — X reaction since the delay announcement

Interactive, self-contained visualisations of how X (Twitter) reacted after [@RaymanGame announced](https://x.com/RaymanGame/status/2099528603335635178) on 14 Sep 2026 (16:00 UTC) that **Rayman Legends: Retold** (Ubisoft's remake) was delayed from 1 Oct to 3 Dec 2026, despite having gone gold.

Live site: https://richardckain.github.io/rayman-legends-coverage/

| Page | What it shows |
|---|---|
| `index.html` | Hub: headline stats and links to every view |
| `network.html` | Animated interaction network (quotes, @mentions, sampled reposts) over time |
| `river.html` | Sentiment streamgraph over time (6-hour / daily, raw or follower-weighted) |
| `bubbles.html` | Reach vs sentiment, one bubble per account |
| `meme.html` | Genealogy of the "2013 vs 2026, delayed next to GTA again" meme |
| `heatmap.html` | Topic x week / day heatmap |
| `cascade.html` | Cumulative reaction curves with t50 / t90 after the delay and the Sep 22 trailer |
| `languages.html` | Sentiment and volume by post language (language as a proxy for region) |

Every page is a single static HTML file with D3 and the data inlined, so it works offline.

## Data and method caveats

- **Window:** 14 Sep 2026 16:00 UTC (the delay post) to 8 Oct 2026 16:28 UTC. 1,742 original and quote posts from 1,165 accounts matching "Rayman Legends", #RaymanLegends, #RaymanLegendsRetold or from:RaymanGame; reposts and replies are excluded.
- **Network links are interactions, not follows:** A → B means B quoted A, @-mentioned A, or appears in a sampled reposted-by list. Follow graphs were not available.
- **Sentiment, topic, delay-relatedness and (where the API omitted it) language are model-assessed** by reading each post; treat them as indicative. Official Ubisoft/Rayman accounts are excluded from sentiment aggregates.
- **Follower counts are as of 8 Oct 2026**, not at posting time. Engagement and impressions are fetch-time snapshots; impressions are a lower bound.
- **Language is not location:** X provides no location, so the map paints each language onto the countries where it is the majority language.
