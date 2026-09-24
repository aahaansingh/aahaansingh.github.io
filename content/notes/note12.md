+++
title = "A PSA on Quantifying the Unquantifiable"
author = ["Aahaan Singh"]
date = 2026-09-24
tags = ["from-beyond"]
categories = ["library", "tech"]
draft = false
+++

There's no good way to organize the links this time.

[Stop Nit-Picking](https://chicagomaroon.com/53643/viewpoints/stop-nit-picking/): Hey!
Read my new article in the Maroon!

[Stop Panicking About AI](https://www.thebignewsletter.com/p/is-artificial-intelligence-going): Sums up my thoughts on the recent AI safety buzz, pretty much.

[Catfishing](https://catfishing.net/): This website is responsible for reuniting my high school quizbowl team after four years, over the course of which I asserted to my friends multiple times that quizbowl is a stupid pastime.
So it is very powerful.
I had this idea once that the sort of people who play quizbowl have brains that are structured like Wikipedia because they are really tickled by making associations between different facts or categories.
They are always hyperlinking.
Catfishing is not about tricking people into thinking that you’re hot, but it is about guessing a Wikipedia article from its tags, so it’s the same type of knowledge game as quizbowl but even more hyperlink-y.
This is why it is like crack for my friends and I.

[Blood Boy](https://granta.com/blood-boy/): I think that this story is very grotesque and it’s really funny that the author not only comes from exactly the same background as everyone in the story, but still works in that space.
It’s basically “what I don’t like about the bay” distilled and I feel bad that I’m plugged in enough to laugh at this while not actively being a part of the strange little society of this piece.
I am in the worst of both worlds but I got to read this.

[Design The Next iPhone](https://neal.fun/design-the-next-iphone/): Go make a helicopter phone.

[Fluoddity](https://fluoddity.com/?name=Shared-Tangle#b=AQgBAAAAAGAOLe4_AAAAAAAA8D8BFW8Wv4B9K7-6u1m_wcQTvyZ9Lb9XkMQ_jiupPYlwxL4F2Le-johvPsXIYD8QNdm-gO0Bvyv3EcBDtUW_UoVuvqjhzb31_p2_OyPaP_-PqL93bh69jyFzvzKWvL-p56K_eQndvf75jr8R3Iw_-F0mv58_Oj5uXTY_mcKov33gAMAFoQo-XJqHvozwqL9PMnw-iM7Uv6rApz_lE8M-Xjnvv5E2jT-q3T8_Pgw7P53olr5Wfjy_Bpr9vq0vHb5zwAhAvc8EP7lZ0j72D1O_6YW6v3Ri6D8hGDG_90Cev7XkNb_x68i-ZtihPRGvhD5Z12g_zxayPw-cDL_wWRNA02iSPzA1VT4HN_6-Xj0FP96ijz_w7rY_Sa9ePzuC2z8ZwD-_BGEVv4seRr8Vgp6862NyP_z19L6-MiE_AAz3PWsK3L8AAADgTWIRQAAAAADXo8C_AAAAgD818D8AAAAgXI_SPwAAAOB6FO4_AAAAAAAAwD8AAADAyqHFPwAAAAArh5Y_AAAAINnOx78AAAAAAAAAAIL3elzFJdI_AAAAAAAAAAAAAAAAAAAAAAAAAAAAAOA_AAAAAAAAAAAAAAAAAAAAAAkAAAAAAAAAAAA): I am not sure what this but you should check it out and make weird shapes!
Feed your joy and enhance your whimsy!

[Napoleon Was The Best General Ever](https://towardsdatascience.com/napoleon-was-the-best-general-ever-and-the-math-proves-it-86efed303eeb/): I used to see a lot of this kind of stuff back when I was a freshman who wanted to do “plot lines on a chart” data analysis because I had no understanding of the world.
So maybe it makes me mad because I’m reminded of my own former smugness and belief in the idea that everything can be easily quantified.
It’s also the kind of project that somebody who’s logged too many hours on Paradox games made which, again, reminds me of the negative qualities of my high school self.
This is personal!
And to those who say that this is such an easy target that it’s not even worth engaging with, I wish that this were the case but I have seen this article shared uncritically on multiple occasions.

So let’s take a look at the methodology.
The metric of interest is WAR for generals, half because it’s easy to digest and half because it’s a good pun.
Fair enough, but this is a complicated metric.
You need good data on army sizes and terrain and morale and you need to somehow quantify a “replacement level” leader in a setting where binning one commander for another would be really disruptive.
In essence, it’s really really hard to create a clean counterfactual.

This is not helped by the dataset, which is just a list of 3580 battles and 6619 generals from Wikipedia.
That’s hardly any data, even if we account for the long tail in the distribution of battles per general.
Furthermore, battles found in the historical record are already going to be biased in favor of the overall victors (a pharaoh wouldn’t make a victory monument to his losses), and the Wikipedia selection will be even more biased by both the amount of data available for a given battle and how interesting the population of Wikipedia battle writers finds a given battle.

Next, the author attempts to regress battle outcomes against relative strengths in infantry, cavalry, artillery, air force, and navy.
They don’t make a distinction between different eras or locations or terrains at all.
They are equating, for example, Mongol cavalry with WWI cavalry in relative effectiveness.
Naturally, the poor fellow couldn’t find much of a signal at all, which they admitted but then glossed over like it didn't invalidate the whole program.
Since the final distribution of general WARs appears
{{< sidenote "normal," >}}Naturally, they didn’t actually test this, not that it necessarily means anything in the first place!{{< /sidenote >}}
however, they claim that the methodology is sound.

Napoleon is found by this method to be the greatest general ever, likely because we have meticulous documentation of all of his victories.
The example given in explaining the metric is the Battle of Borodino, in which he “defeats” the Russian army, earning him .49 WAR.
This is a great example of another reason why the system sucks, which is that we can’t even define what a victory or defeat is.
The Russians may have left the field at Borodino, but they set in motion the ruination of the French army.
Napoleon’s poor decisions in Russia, insofar as they could have affected the course of the army, are not covered by this metric at all.
Most of his losses were to hunger and the cold, but they are not accounted for in battle.
In any case, I don’t think that generals matter very much at all, and much ink has been spilled on how this is the case in Napoleon’s Russian Campaign in particular—most famously, _War and Peace_.

[gzip-lm](https://nathan.rs/posts/gzip-lm/): Here’s a fun little experiment.
I aspire to do something like this on the blog someday.

[Paid Phones](https://thebaffler.com/salvos/paid-phones-kolitz): Payday lending is one of the most repugnant legally sanctioned forms of financial extraction.
I can’t even laugh at this essay, it’s just sad.
