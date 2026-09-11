# Week 8 — Style mixer ships, memory woes hit

_Published: 2026-09-11_

Hey everyone,

This week we finally shipped the new style mixer feature. Users can now blend two reference styles (think "cyberpunk + watercolor") in a single prompt and get coherent results without heavy post-processing. Early feedback has been solid—conversion rates on the portrait generator jumped about 18% since launch.

We also hit a fun challenge: the new mixer doubled our VRAM usage during inference. A few production runs OOM'd on the smaller GPUs, forcing us to hot-patch a fallback path mid-week. It wasn't pretty, but it forced us to finally instrument the memory profiler we've been putting off.

Next up we're tightening the prompt parser so mixed styles respect user weighting more reliably, plus we want to cut cold-start latency by another 30%. 

Thanks for following along—building this in public keeps us honest.

[AdLoft](https://adloftai.com/blog/ai-portrait-photo-any-style.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)