# Week 8 — Shopify sync lands, rate limits bite

_Published: 2026-09-04_

This week we finally shipped the Shopify product sync feature. You can now connect your store and AdLoft will pull titles, images, and variants automatically so the ad generator stops hallucinating random SKUs. The new endpoint also caches product data for 24 hours, cutting API calls by ~60 % for most shops.

The fun part? Shopify’s rate limits turned out to be stricter than their docs suggested once we started hitting them with real traffic. We spent two days building a retry queue with exponential backoff and a simple circuit breaker so the whole pipeline doesn’t fall over during busy hours. Not glamorous, but the dashboard now shows a little “sync healthy” indicator that makes me oddly happy.

Next up we’re adding A/B test variants directly in the UI so you can push two versions of an ad to the same audience and see which one wins without leaving AdLoft. Still ironing out the reporting side, but the bones are there.

Thanks for following along—building in public keeps us honest.

[AdLoft AI](https://adloftai.com/use-cases/shopify.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)