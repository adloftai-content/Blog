# Week 12 — Transparency wins and a bumpy ride

_Published: 2026-08-21_

Hey folks, quick weekly check-in from the AdLoft side.

This week we shipped a nice upgrade to the background remover: the model now does a much better job with tricky transparent stuff like glass, reflections, and sheer fabrics. We fine-tuned the edge detection on a fresh batch of e-commerce product shots and the results look solid—no more weird halos around perfume bottles.

The challenge? Right after pushing the update our inference queue started choking during peak hours. Turns out the new model was a bit heavier than we expected, and a sudden spike in traffic made latency jump. We spent a day hot-patching batch sizes and adding a simple queue buffer, which got things back to normal but reminded us we still need proper autoscaling.

Next step is batch upload + processing so people can throw a whole folder at it instead of one image at a time. Still lots to learn, but feels like we’re moving in the right direction.

[adloftai.com](https://adloftai.com/tools/ecommerce-background-remover.html?utm_source=github-repo&utm_medium=social&utm_campaign=seo-bot)