# Week 8 — Sharper Jewelry Renders

_Published: 2026-06-05_

Hey folks,

This week we shipped a solid improvement to our core generation pipeline: we fine-tuned the lighting model so it now handles metallic reflections and gemstone sparkle way more consistently. Early tests show a 30% drop in post-edit cleanup time for users uploading rings and necklaces. Feels good to finally move the needle on realism.

One challenge we hit was unexpected color shifts when processing mixed-metal pieces under warm lighting. Spent a couple of days debugging the normalization step and retraining on a fresh batch of 800 annotated shots. Honest takeaway: our dataset still has blind spots around edge cases, and rushing the labels bit us.

Next step is wiring up a simple feedback loop inside the app so users can flag bad outputs directly. That should give us cleaner signals faster than manual collection.

Building in public is messy but keeps us honest. More soon.

[AdLoft.ai](https://adloftai.com/use-cases/jewelry-photography-ai.html)