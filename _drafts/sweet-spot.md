---
layout: post
title: Outside The Sweet Spot
---

<img src="/images/sweet-spot.png" alt="band" width="300"/>

A wonderful musician friend of mine, Zane Gill had a saying: "Just because you can doesn't mean you should".  Sometimes in a pinch maybe you can’t help it.  For example, there was that time my daughter and I took a bike trip.  We were running behind schedule (too many “selfie stops”) and it started getting dark.  As luck would have it, both of our headlights died and dad forgot to pack batteries.  Improvising, I used my iPhone light.  We survived of course, but the beam was weak & wobbly.  Clearly not what Steve Jobs had in mind when he added the camera light.

This same principle can apply to your product and the tools / frameworks on which it depends.  Over time, you may find yourself well outside the sweet spot of those dependencies.  This can result in having your team spending more and more time working around their limitations - time better spent adding valuable features to your application.

Moving outside of the sweet spot can take several forms.  Here are a few cases I’ve encountered...

### Not Intended Use

Wikipedia defines stored procedures as useful for “data-validation or access-control mechanisms”.  I worked on a product that went way beyond this and developed a complex calculation engine - all in stored procedures.  Conway’s Law explains why the product evolved in this way - the strongest personalities on the team at that time were database administrators, so they utilized the toolset they knew best.

Like the iPhone headlight, the result was functional but extremely unwieldy.   Debugging code became a nightmare - simple aides like logging - again while possible - were incredibly difficult from inside the database.  Profiling performance became a black art of coaxing the optimizer to better performance.  Just because you can, doesn’t mean you should.

### Outgrown

I recall another project that was using a graphical ETL tool.  At the start, the team loved having a tool that would allow data analysts to create flows without a dependency on engineering, chaining blocks to sort, group, merge and split data.  However, over months the team had built out flows which included thousands of blocks.  It got to the point where simply opening one of these flows in the tool would take minutes.  The tool was not designed with this level of complexity in mind.

Getting and staying in the sweet spot is a challenge for any product team.  New products need to seriously evaluate capability sets for critical tools and frameworks. Once selected, products need to continuously assess whether or not they are outgrowing or abusing these tools. This involves understanding why a given tool was chosen in the first place and determining if the use cases have changed to a point that warrants reconsideration. Abstractions can help ease the pain when it’s time to swap out a key dependency. 
