# Week 12 — Ad variations live and scaling pains

_Published: 2026-05-22_

Hey everyone,

This week we shipped a big upgrade to the creative flow: upload one product shot and the AI now spits out five full ad variations with matching copy, headlines, and platform tweaks. Beta users are already reporting they’re cutting production time in half, which feels like the kind of win we’ve been chasing.

Of course it wasn’t all smooth sailing. We ran into nasty latency spikes once traffic picked up, and it turned out our vector search wasn’t keeping pace with the new dataset size. A couple of late-night debugging sessions later we added aggressive caching and some query pruning—still monitoring, but things are steadier now.

Next on the list is rolling out in-app A/B test automation so users can launch variants and let the system pause the losers automatically. Should be interesting to watch the data roll in.

Building in public means sharing both the shiny bits and the bumps—thanks for the continued feedback!

[AdLoft.ai](https://adloftai.com/alternatives/photoroom.html)