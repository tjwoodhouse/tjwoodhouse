---
title: Cartion Ai and Bible translation into gateway languages
---

One of the major challenges to Bible translation in the era of AI is licenses. We need openly licensed base texts in gateway languages that can serve as input to AI translation tools. 

This allows teams to experiment with AI translation tools without having to go through any kind of request process with a rights holder. Defiantly a plus from my perspective. 

I've been pondering how to do this and I'm playing around with translating the [Open English Bible](https://openenglishbible.org/oeb/2022.1/read/) (OEB) to Bahasa Indonesia using [Carton](https://github.com/VivekPanyam/carton) to run Facebook's M2M 100 model.

OEB is CC0 i.e. public domain, meaning we can do whatever we want to with it and don't even have to credit them, though I think that should be done so the chain of translation is clear. The World English Bible is also public domain and would be a possible input candidate as well.

The code is pretty simple, but there are a few issues. M2M 100 deletes the USFM markup or does odd things with it so I had ended up having to split the USFM out and translate each line individually. But it seems to do an ok job. I've seen some things that will need to be fixed, but I imagine that more post processing for certain phrases should be enough to get a reasonable starting point. 

If you speak Indonesian, you can check out the output [here](https://github.com/tjwoodhouse/open-Indonesian-Bible). There is SFM and also pdf output (built using Typst)
