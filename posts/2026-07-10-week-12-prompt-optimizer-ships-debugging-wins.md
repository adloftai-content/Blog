# Week 12 — Prompt optimizer ships, debugging wins

_Published: 2026-07-10_

This week we finally shipped the new prompt optimizer for our cosmetics photography pipeline. It now auto-tweaks lighting keywords and skin-tone references based on product metadata, cutting average generation time by ~30% and reducing the “too shiny” artifacts users kept flagging.

The biggest challenge was an edge case where metallic packaging kept triggering weird color shifts. Spent two late nights tracing through the diffusion scheduler before realizing we’d accidentally doubled the guidance scale on metallic prompts. Classic.

Next step: adding batch-upload support so creators can queue an entire campaign in one go. Still ironing out the queue logic, but excited to get it in front of early testers.

[AdLoft](https://adloftai.com/use-cases/cosmetics-photography-ai.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)