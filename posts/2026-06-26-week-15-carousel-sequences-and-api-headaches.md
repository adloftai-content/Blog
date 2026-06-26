# Week 15 — Carousel sequences and API headaches

_Published: 2026-06-26_

Hey everyone, Week 15 at AdLoft was a mixed bag of shipping momentum and real-world friction.

The highlight was finally shipping the carousel sequence generator. It now takes a product image + short brief and outputs a 5-slide story flow with suggested captions and CTAs. Early alpha users are seeing 2x faster creation time and a noticeable lift in engagement on test posts. We leaned hard into chain-of-thought prompting and a small curated dataset of high-performing carousels to get the narrative arc right.

The challenge came from Instagram’s Graph API throttling. What should have been a quick data sync turned into multi-hour delays and some manual retries. We learned the hard way that optimistic rate-limit assumptions break fast when you’re pulling historical ad performance at scale. A quick Redis-backed queue and exponential backoff helped, but it cost us two days of polish time.

Next up we’re wiring in direct A/B test reporting so users can compare variations inside the dashboard instead of exporting CSVs. Should ship that in the next sprint.

[adloftai.com](https://adloftai.com/use-cases/instagram-ads.html)