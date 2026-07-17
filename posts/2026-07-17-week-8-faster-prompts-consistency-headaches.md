# Week 8 — Faster prompts + consistency headaches

_Published: 2026-07-17_

This week we shipped an upgraded prompt router that trims average generation time by ~30 %. The change came from pruning a bunch of redundant tokens and adding a lightweight style cache; early tests show the outputs still feel fresh while burning fewer credits. Along the way we learned how much a single well-placed negative prompt can save us from weird anatomy fails.

The stubborn challenge was (and still is) cross-angle character consistency. We tried a few lightweight conditioning tricks, but under tricky lighting the faces still drift. It’s humbling to watch a model nail the outfit yet swap jawlines between shots.

Next step: wire up an in-app thumbs-up/down loop so we can collect real user preferences and feed them back into prompt scoring. Should give us better signal than our internal evals.

[adloftai.com](https://adloftai.com/blog/ai-influencers-without-lora.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)