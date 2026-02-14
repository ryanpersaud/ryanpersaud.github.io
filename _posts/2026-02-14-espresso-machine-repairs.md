---
layout: post
title: "Surgery on a Diletta Mio"
date: 2026-02-14 08:00:00 -0600
categories: [Hardware]
tags: [espresso, repair]
---

*Disclaimer: Aside from the following disclaimer content, the content of the post is solely from my brain and not the product of AI.  This post is a summary of my personal experience repairing my own espresso machine. I am not a professional technician. Espresso machines involve high temperatures, electrical components, and pressurized water. Any repairs you undertake are at your own risk. If you are unsure about what you are doing, consult a qualified repair professional. You should validate that any parts are appropriate for your machine before installing them!*

In November of 2022, we bought a Diletta Mio espresso machine. We figured with the amount of lattes that we buy from Starbucks, the machine would pay for itself in short order. This proved to be true, and we have been enjoying lattes, steamers and espresso martinis for the last few years. Most mornings, I get up and make some variety of pourover for Erin and me. As I'm wrapping up the process, I hit the power switch on the espresso machine so that it's fired up and ready to go (like we were circa 2009).

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/fired-up-ready-to-go.jpg" alt="The author fired up and ready to go in January 2009" style="width: 52.5%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">The author fired up and ready to go in January 2009</p>
</div>

One morning last year, I went through my normal routine, but when I hit the power button the machine briefly turned on (I could hear the relays click) and then turned off. After some more futzing, I realized that the power switch was not latching like it was supposed to (it was acting like a momentary switch). Erin emailed Seattle Coffee Gear who distributed the machine about the situation, but they weren't particularly helpful (they wanted our SCG order number which we didn't have since we bought it from another online store). She also trawled the machine's Facebook page, but did not find anything related to the power switch.

Eventually, we took the top off the machine and I started poking around. After going down several rabbit holes and learning far more about Normally Open/Normally Closed switches than I wanted to, and trying to find a replacement switch on Mouser and Digikey, I hit the motherlode with AliExpress. I had previously only purchased an el cheapo wifi adaptor for a desktop computer from AE, so I was not fully aware of the breadth of electrical components that were available on the site. There were many options that seemed like they could work, so I found one that matched the aesthetic of our existing switch and also had similar current and voltage ratings. Here's the [model](https://www.aliexpress.us/item/2255801081677336.html) I ended up ordering, though I don't know what the lifespan of that link is. There are a number of options from that page, and I went with "Ring-Blue, Silver-Latching, 220V, 2NO2NC" and it cost $8.64 with shipping. It took a few weeks to arrive, and, when it did, I popped the old wiring harness onto it, and the machine fired up without any issues.

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/espresso-power-button.jpeg" alt="Replacement power button installed on espresso machine" style="width: 52.5%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">I didn't get an exact match for the color, but it does the job.</p>
</div>

We continued making our tasty hot beverages for a few months, but then the steam wand stopped making steam and just dripped water. After some investigation on the aforementioned Facebook group, Erin determined that a thermostat was being tripped and learned how to reset it. As everyone does when a home appliance is acting up, we hoped it was an isolated incident. Unfortunately, as is often the case, the thermostat kept tripping.

When I dug into the thermoblock design a bit more, I learned that there are two thermostats, one is a "[snap-action, bimetal disc thermostat used for temperature control](https://www.calcoelectric.com/thermostats/bimetal-thermostats/258-ksd301-series-bimetal-thermostat#:~:text=KSD301%20series%20snap%2Daction%20bimetal%20thermostat%20is%20a,to%20provide%20temperature%20control%20or%20temperature%20protection.)" and the other one (the one that Erin had to reset) is a [bimetallic thermostat with a manual reset](https://vikiwat.com/en/bimetal-thermostat-271oc-nc-16a-250vac-a2-013r-leads-2x6-3mm.html?srsltid=AfmBOoqTfhiaITxCFIrRKtGvNCFj_-xsdVuC-sJ9QBn_ji2BHEXIozci). My understanding is that the first thermostat is responsible for regulating the temperature of the thermoblock by cutting power when the desired temperature is met, and, if it fails in this duty and the temperature continues to rise, then the second thermostat will eventually be triggered and cut power to the thermoblock.

It seemed best to replace both thermostats so I started googling the model numbers on the thermostats. I found devices that looked similar, but I wanted to have more confidence that I was ordering the correct parts for our machine. I looked at the Seattle Coffee Gear site, but there was no mention of thermostats, so I threw some more incantations into Google involving thermoblock, Diletta Mio, thermostat, etc. One of them uncovered [this](https://www.reddit.com/r/espresso/comments/1h5yewy/comment/mmrr2yv/?force-legacy-sct=1) Reddit thread where someone's primary thermostat (the first one I mentioned) was significantly damaged. Interestingly, their power switch also failed previously, and they also had no luck with SCG support. The user mentioned that the Diletta Mio is manufactured by [Quickmill](https://www.quick-mill.com/) and is related to the Silvano Evo. Another user suggested contacting Chris's Coffee since they are the Quickmill distributor in the US, and it turned out that Chris's carried [the replacement thermostat](https://www.chriscoffee.com/collections/quick-mill/products/qm-silvano-steam-bank-thermostat-160). I ordered that and [a replacement for the second thermostat](https://www.chriscoffee.com/collections/quick-mill/products/qm-silvano-steam-bank-resettable-thermostat-220c) for $40.35 with shipping. They arrived within a few days and I was able to swap out the old parts with the new ones without too much trouble. So far, so good - we're back to enjoying our daily lattes and steamers.

<div style="display: flex; justify-content: center; align-items: flex-start; gap: 1em; margin-bottom: 2em;">
<div style="text-align: center;">
<img src="/assets/images/old-espresso-thermostats.jpeg" alt="The old thermostats" style="height: 300px; width: auto;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">The old thermostats</p>
</div>
<div style="text-align: center;">
<img src="/assets/images/hunter-steamer.jpg" alt="Hunter enjoying a steamer" style="height: 300px; width: auto;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">A gingerbread steamer</p>
</div>
</div>
