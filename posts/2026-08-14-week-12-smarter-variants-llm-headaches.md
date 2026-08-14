# Week 12 — Smarter variants & LLM headaches

_Published: 2026-08-14_

This week we shipped a small but useful improvement to the ad variant generator. Instead of spitting out generic copies, the engine now pulls in more context from product pages and generates three distinct tones (benefit-focused, urgency-driven, and story-style) in a single pass. Early users noticed the output felt less repetitive, which is exactly what we were going for.

The challenge came from trying to speed things up. We switched to a faster model for the first pass and immediately hit inconsistent brand voice—some outputs started sounding like they were written by a very enthusiastic salesperson from 2012. Spent a couple of days iterating on system prompts and adding a light post-processing step to catch tone drift. Learned (again) that faster isn't always better when you care about quality.

Next step is adding basic image-suggestion logic so users can see rough visual directions alongside the copy. Still figuring out the right guardrails, but excited to ship something tangible.

[AdLoft AI](https://adloftai.com/use-cases/amazon.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)