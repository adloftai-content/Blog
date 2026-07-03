# Week 12 — Bulk variations and rate-limit reality

_Published: 2026-07-03_

This week we shipped a bulk generation mode for eBay reseller listings. Users can now queue up to 50 images at once with shared style presets (think “bright lifestyle” or “clean white background”), and the system handles deduping and folder exports automatically. Early feedback shows it cuts listing time in half.

The big challenge was hitting OpenAI’s image API rate limits hard once the queues grew. We spent two days adding backoff logic and a simple priority queue so paid users don’t get starved by free-tier traffic. Not glamorous, but it’s shipping today.

Next up: adding in-app A/B test tracking so sellers can see which variation actually sells better instead of guessing.

[AdLoft AI](https://adloftai.com/use-cases/ebay-reseller-photos-ai.html)