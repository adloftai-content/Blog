# Week 8 — Shipping better food lighting + wrestling with rate limits

_Published: 2026-07-31_

Hey folks, quick weekly check-in from the AdLoft crew.

This week we shipped a lighting-enhancement pass on our food-photography pipeline. Prompts now automatically detect plate angle and add subtle rim lighting plus soft fill, which has lifted average aesthetic scores in our internal evals by ~18 %. We also exposed a new “mood” slider in the UI so users can dial between cozy and clinical without rewriting prompts.

The biggest headache was an unexpected rate-limit cliff from our primary image model. We hit it hard on Tuesday night during a test batch of 400 variations; the queue backed up and a few jobs timed out. We spent the rest of the week adding exponential back-off, request batching, and a small fallback model. Not glamorous, but the reliability graph looks a lot better now.

Next up we’re wiring in a simple thumbs-up/down feedback loop so the model can learn which lighting combos actually convert for real campaigns. Should be live by mid-next week.

As always, feedback welcome—open an issue or ping me directly.

[AdLoft.ai](https://adloftai.com/use-cases/food-photography-ai.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)