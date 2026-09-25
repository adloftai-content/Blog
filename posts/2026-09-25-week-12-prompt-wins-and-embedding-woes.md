# Week 12 — Prompt wins and embedding woes

_Published: 2026-09-25_

This week we shipped a solid improvement to the core ad copy generator. By swapping in a handful of curated industry examples and tightening the system prompt structure, output relevance jumped noticeably. Early testers are seeing more punchy hooks and fewer generic lines, which feels like real progress on the quality front.

The challenge came when we tried bolting on a vector store for campaign memory. Embedding mismatches kept surfacing, and query latency spiked under even moderate load. Spent two days tracing token counts and chunking logic before landing on a workable (if still clunky) fix. Classic "it worked on my machine" moment.

Next step is wiring direct thumbs-up / thumbs-down feedback into the generation loop so the model can adapt faster from real edits. Should ship a rough version next week.

[AdLoft](https://adloftai.com/tools/?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)