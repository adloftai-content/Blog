# Week 15 — Faster renders and prompt headaches

_Published: 2026-08-28_

This week we shipped a solid improvement to the core mockup pipeline: switched to a lighter diffusion model variant that cuts generation time from ~12s to ~7s on average while keeping visual quality basically the same. Early user tests on the staging site have been positive, especially for quick iteration loops.

The challenge was prompt drift on complex product angles. The new model sometimes ignored material details we explicitly passed in, forcing us to spend a couple of days rebuilding the prompt layer with more structured JSON inputs instead of free text. Not glamorous, but necessary.

Next step is adding a simple batch queue so users can queue 5–10 variants at once without hammering the API. Should ship that in the next few days.

[AdLoft AI](https://adloftai.com/blog/how-to-create-product-mockups-with-ai.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)