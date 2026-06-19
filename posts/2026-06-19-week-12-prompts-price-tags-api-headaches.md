# Week 12 — Prompts, Price Tags & API Headaches

_Published: 2026-06-19_

This week we shipped a meaningful improvement to the price tag generator. We rewrote the core prompt chain to pull real product attributes (size, color, margin) directly from user uploads instead of relying on generic placeholders. The result is tags that actually look native to the product photos rather than slapped-on afterthoughts. Early internal tests showed a nice bump in visual coherence.

The not-so-fun part was wrestling with rate limits on the new image model we integrated. We burned through our quota twice in one day and had to hot-patch a simple retry + backoff layer at 2 a.m. It reminded us how fragile these pipelines still are when you’re building in public with third-party APIs.

Next step is adding Shopify one-click export so merchants can push the generated assets straight into their product pages without downloading anything. Should ship that next week.

[adloftai.com](https://adloftai.com/blog/ai-price-tag-generator-product-ads.html)