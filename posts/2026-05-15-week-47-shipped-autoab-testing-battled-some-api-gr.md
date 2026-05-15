# Week 47 — Shipped auto-A/B testing + battled some API gremlins

_Published: 2026-05-15_

# AdLoft Weekly Dev Update: Week 47 🚀

Hey build-in-public fam! Another week in the books at AdLoft AI. We're cranking on making ad creation dead simple for indie hackers and marketers who hate designers (like me). Here's the rundown:

## What We Shipped ✨

**Auto-A/B Testing Dashboard is live!** 🎉 Now when you generate ad creatives, AdLoft automatically spins up 3-5 variants and runs them head-to-head in your ad accounts (FB/TT/LinkedIn). See click-through rates, conversions, and a clear winner in ~24hrs. No more manual variant hell. Early users are seeing 20-30% uplift already. Tried it on a coffee brand this week—variant #3 crushed it with emoji-only headlines.

## The Challenge We Tackled 💥

Meta's API decided to throw tantrums mid-week. Rate limits spiked, auth tokens expired randomly, and ad approvals got stuck in limbo. Spent 2 days deep in their docs and Slack channels. Honest truth: third-party APIs are the silent killer of SaaS. Fixed it with exponential backoff retries + token refresh logic, but lost a day of dev time. Lesson learned: always have API wrappers with battle-tested fallbacks.

## What We're Building Next 🔮

Voiceover generation for video ads. Imagine uploading a script and getting human-sounding narration in 20+ languages, auto-synced to visuals. Testing ElevenLabs integration this weekend—should ship early next week.

Total lines coded: 1,247. Coffee consumed: 23 cups. User signups: +14% WoW.

Thanks for following along! Questions? Hit reply or Discord.

[adloftai.com](https://adloftai.com/blog/how-to-make-ad-creatives-without-designer.html)