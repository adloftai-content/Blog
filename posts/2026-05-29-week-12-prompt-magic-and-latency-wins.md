# Week 12 — Prompt Magic and Latency Wins

_Published: 2026-05-29_

Hey team,

Shipped a big upgrade to our core prompt optimizer this week. It now auto-tweaks lighting, plating angles, and color grading suggestions based on the dish type—think better steam highlights on ramen or that perfect golden crust on pizza. Early tests show a 25% lift in "appetite appeal" scores from our internal eval set. Also squeezed out ~180ms average latency on the image gen pipeline by swapping in a lighter upscaler and caching some embeddings.

Biggest challenge: we hit a nasty edge case where certain ingredient combos (looking at you, glossy sauces) kept triggering weird artifacts. Spent two days chasing it through the diffusion steps before landing on a quick mask-based fix. Felt slow, but honest debugging beats shipping broken pixels.

Next step is wiring up a lightweight feedback loop so users can thumbs-up/down outputs directly in the UI and we can retrain the optimizer faster. Should be live by mid-next week.

Building in public means showing the bumps too—more soon.

[AdLoft.ai](https://adloftai.com/use-cases/food-photography-ai.html)