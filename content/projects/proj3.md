+++
title = "This Website"
author = ["Aahaan Singh"]
date = 2026-04-15
categories = ["design", "tech"]
draft = false
+++

This is a Hugo website using [my fork](https://github.com/aahaansingh/hugo-theme-til) of the [Today I Learned](https://github.com/michenriksen/hugo-theme-til) theme.
It used to look like [this](https://web.archive.org/web/20250601000000*/aahaansingh.github.io), and then like [this](https://web.archive.org/web/20260402031134/https://aahaansingh.github.io/).
The first iteration was the original theme, which is very well-designed.
I originally chose it because I thought that the graph (which I didn't learn until later was an Obsidian feature) was cool, but there are many other reasons to like it:

-   The Posts/Notes division is a useful way of organizing blogs by effort.
-   The sidenote implementation is excellent, and, as regular readers (myself) of this blog know, sees a lot of use. In fact, sidenotes have probably improved the quality of my prose because they enable me to shift tangentially-related observations out of the main body.
-   The theme does a good job linking posts together, both by relating on tags and through the graph.

The original structure of the theme has largely been preserved and, as it is the most important component of this website, the majority of the credit for the design as it currently exists goes to the [author](https://michenriksen.com/).

The modifications made in the second iteration are entirely stylistic.
At the time, I was not very well versed with CSS, didn't know what Tailwind was, and had no clue how Hugo's HTML worked.
As such, this restyling is somewhat clunky at the code level and I wasn't able to incorporate some features that I really wanted.
Furthermore, the design choices that _were_ implemented are somewhat questionable.
I like Baskerville for body text, but [Avería Serif](http://iotic.com/averia/), despite having a lot of character, looks sloppy in this application.
Color-wise, the red accent is overused and the light blue background is harsh on the eyes.
I have also noticed that many people find it entirely indistinguishable from white.

The current iteration of this website fixes most of these problems.
The colors are, in my opinion, more tastefully and broadly applied.
I took inspiration from control room color coding, as described [here](https://bethmathews.substack.com/p/why-so-many-control-rooms-were-seafoam).
Beige backgrounds are a bit [generic](https://joinreboot.org/i/182220227/out-beige-microsites) in this day and age but I feel that there are enough splashes of color to keep the site visually interesting.
I also switched to more [professional-looking](https://practicaltypography.com/free-fonts.html)
{{< sidenote "fonts." >}}Other decisions like the post titling, link formatting, and line length, were also taken from Butterick's recommendations/work.{{< /sidenote >}}
Issues on mobile have been fixed, and there is now a proper [Projects](https://aahaansingh.github.io/projects/) page.
That is presumably how you got here.

I have no plans to make major changes to this site's design, but if I ever become competent at webdev (unlikely), I may give it a second look.
