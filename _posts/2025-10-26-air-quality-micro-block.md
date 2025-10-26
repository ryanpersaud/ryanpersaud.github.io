---
layout: post
title: "Air Quality Micro Block"
date: 2025-10-26 12:39:11 -0600
categories: [IoT, Hardware]
tags: [air-quality, micro-block]
---

A few weeks ago, I accompanied Erin to her 25th reunion at Colorado College in Colorado Springs. They are one of a few schools that have the block plan where instead of taking multiple classes throughout a semester, students take one class at a time for three and a half weeks. This means that students have concentrated deep-dives into subjects - it definitely seems to resonate with some students more than others. I'm still not sure if it would suit my learning style. I like to deep dive on various topics, but I also recognize that sometimes I need time to internalize material. During the reunion weekend, Micro Blocks were offered where attendees could get quick exposure to a subject. I decided to take a Micro Block on Air Quality, and it ended up being quite interesting.

The Micro Block was led by a [Dr. Andrea Bruder](https://www.coloradocollege.edu/basics/contact/directory/people/bruder_andrea_s.html), a professor of Mathematics and Computer Science. Like many folks, she got interested in Air Quality during the pandemic. Rather than trying to regurgitate the content verbatim, I am going to focus on the areas that I found notable.

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/filter-petri-dish.jpg" alt="A bear coding with good vibes" style="width: 52.5%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">A sample taken from an indoor air filter and grown in a petri dish</p>
</div>

Dr. Bruder swabbed an air filter from an HVAC system and grew the sample on agar (see above picture). It should not have been a surprise, but it was kind of shocking to see what grew out of normal indoor air. Mara did a similar experiment recently where she swabbed classmates' and teachers' computers and saw what grew from the samples. The results in that case were a little more understandable since it's easy to picture all the bacteria living on a keyboard. 

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/outdoor-air-reading.jpg" alt="A bear coding with good vibes" style="width: 70%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">Taking outdoor readings</p>
</div>

It was helpful to review what PM2.5 (particulate matter 2.5) means (I often forget the precise definition). It's a measurement of the particles that are 2.5 micrometers or smaller in the air. The first thing that I typically forget is that it's not just particles that are 2.5 um in diameter, it's <= 2.5μm. It's also important to note that rather than a count, PM2.5 is a measurement of the mass of such particles in a given volume, specifically μg/m3. One implication of this definition is that PM2.5 value depends on not just the number of particles in the air, but also the mass of the particles. Most Indoor Air Quality (IAQ) devices that I had previously used had PM2.5 and maybe PM1, but during the Micro Block, we got to use some devices that measured the count of particles of various sizes.

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/corsi-rosenthal-pc-fans.jpg" alt="A bear coding with good vibes" style="width: 52.5%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">Corsi-Rosenthal box in with PC fans in the classroom</p>
</div>

During the pandemic, [Corsi-Rosenthal boxes](https://en.wikipedia.org/wiki/Corsi%E2%80%93Rosenthal_Box) were a popular, relatively inexpensive way to filter the air in spaces like classrooms to remove Covid virus particles. I had heard of them and seen a few different models online, but I did not realize that Jim Rosenthal was a Colorado College alum. The design has continued to evolve and new models now use PC fans instead of box fans to move air through the box (see above). PC fans are quieter and more energy efficient than box fans, though box fans can generally move more air. Corsi-Rosenthal boxes use less energy and are quieter than HEPA filters, and, since they can move a large quantity of air per minute, they can still [get to ISO clean room standards](https://www.texairfilters.com/could-corsi-rosenthal-boxes-reduce-particles-to-cleanroom-levels/) (with multiple air changes per hour). Jim Rosenthal will be co-teaching a [half block course](https://today.coloradocollege.edu/announcements/32948) with Dr. Bruder on Environmental Health & Indoor Air.

<div style="text-align: center; margin-bottom: 2em;">
<img src="/assets/images/particle-size.png" alt="A bear coding with good vibes" style="width: 52.5%;">
<p style="font-style: italic; color: #666; margin-top: 0.5em; font-size: 0.9em;">Fractional collection efficiency versus particle diameter for a mechanical filter (<a href="https://www.cdc.gov/niosh/docs/2003-136/pdfs/2003-136.pdf">source</a>)</p>
</div>

Perhaps the most interesting fact I learned during the session was about particles that are .3μ in diameter. Counterintuitively, they are harder for most filters to capture than particles with smaller diameters since smaller particles exhibit [Brownian motion](https://en.wikipedia.org/wiki/Brownian_motion) and the zig-zag paths that they traverse make them more likely to be trapped by filters.
