+++
title = "Celadon v0.1.0"
author = ["Aahaan Singh"]
date = 2026-03-18
tags = ["i-did-a_thing"]
categories = ["tech"]
draft = false
+++

Ideally an app would be its own justification, but there are so many dang RSS readers out there that there is nothing inherently interesting about making yet another one.
I am flattering myself by considering my own app, [Celadon](https://github.com/aahaansingh/Celadon), to be of sufficient interest, but clearly I believe in it if I made it.
I would like to discuss how and why.

I can't quite recall how I came across RSS, because nobody I know uses the technology.
That is a shame.
It's amazing that you can collect most of the things that you read on the internet in a unified interface at zero cost—that ethos is nearly a relic of the past.
Social media, however, is a ubiquitous alternative that takes far less effort to consume because it turns curation into a background task.
It has therefore gouged out a big chunk of the prospective RSS userbase.
The advantage of RSS, though, is that it's not inherently algorithmically driven.
There is no agenda or black box mediating your access to information.

This is important, because with any tool, there is a temptation to overcomplicate things.
RSS is especially prone to this—it is such a simple concept that developing a new reader risks squaring the wheel.
There are a gajillion readers these days that try to integrate AI or employ some sort of algorithmic approach to content delivery, but I don't believe that such features are necessary when their ultimate realization already exists.

Of course, this is a very convenient position for me to take.
I have never made an app before, so a simple reader is low-hanging fruit.
All you need is to store feeds, send requests, and have some sort of UI.
This is what initially made the project so appealing to me when I decided, last year, to work on a project of some significance.
On top of that, Tauri makes packaging desktop apps very easy _and_ lets you develop in Rust.
I'm not very good with Rust but I like it, as does
{{< sidenote "everybody else." >}}My programming languages professor approvingly referred to it as a language designed by people with a great understanding of type theory, and I'll take his word for it.{{< /sidenote >}}
My original plan was to make an extremely simple inbox-style reader with in-app article display—essentially, [Feeder](https://feeder.co/) but with an unlimited amount of feeds and articles.
Since I'd just come off my [cricket stats](https://aahaansingh.github.io/projects/proj1/) project, I had the idea that I could integrate some analytics into the software: most read feeds, average read time, keywords, etc.
Really, I just wanted to get something out there that was good enough for me to use.

_That_ motivation carried me through the planning process and the entire backend, which took about two months.
Once I had a working model, though, I stalled out.
I didn't know any frontend frameworks, had no desire to learn any, and had no incentive to learn either because I no longer saw the point in making a worse version of an existing tool.
I had other fish to fry over the summer, so the project fell off my radar entirely.

A couple of things changed between last year and last month.
For one, AI tools have gotten to the point where they can code decent-looking frontends just by using drawings as a reference.
Another factor was that I came across Terry Godier's recent [essay](https://www.terrygodier.com/phantom-obligation) in which he questions the current paradigm of readers-as-inboxes.
This design, so familiar that it is not even recognized as a choice, is deeply embedded in the history of the reader and to this day, pretty much every popular reader looks the same.
They are not the only way, however, to aggregate and deliver content.
Social media platforms don't have unread counts because that would be stupid—there's just so much information out there that an unread count is meaningless.
RSS readers sit in between the two, because while the user picks and chooses where they are getting their information from, they have no inherent need to read every article from every page that they are subscribed to.

Here's an instructive example.
I used to listen to music for seven hours a day, and had a [last.fm](https://www.last.fm/) tab pinned on my browser.
Every Friday without fail, I would check my weekly listening report and feel good about myself for listening to 800 songs in a week.
Sometimes, I would accidentally-on-purpose leave Spotify playing on my headphones while I was falling asleep, which is counterproductive because listening to music keeps me awake.
However, doing so enabled me to increase my listening count, on the off-chance that I forgot to turn my headphones off.
These days, I listen to way less music but find myself enjoying it a lot more.
I also never check my last.fm because if I did, I would feel bad that my number is smaller now than it was two years ago.
Something as benign as a listening counter is able to drastically influence my consumption habits, and I know that this is pretty common behavior.
Unread counters have a similar effect—they turn reading into a chore in service of clearing the inbox, rather than an end in and of itself.
Since ditching the feature, I have found myself opening fewer articles but reading those articles more closely.

There's a lot more to like about Godier's RSS app, [Current](https://www.terrygodier.com/current).
The most interesting idea to me was auto-expiry: automatically marking an article as read after a set period of time which can be customized by the user.
My biggest problem with RSS readers is that you can't mix high-frequency feeds and low-frequency feeds together.
You are liable to miss your favorite posts by infrequent bloggers if you subscribe to Hacker News.
Auto-expiry solves this because you can expire posts from high-frequency feeds faster, so your main page gives you a far more balanced survey of the information that you're interested in.
It is, essentially, a really simple algorithm that does the job transparently and effectively.

I now realized that Feeder was
{{< sidenote "bad" >}}For me specifically, I think that 95% of people would prefer it over my own reader and would be justified in doing so.{{< /sidenote >}}
and that I had the ability to make something better, so I did, and that thing is Celadon.
I made a few other structural deviations from the norm.
I decided to replace folders with "superfeeds," which are the same thing except feeds can have multiple
(meaning that I have a tagging system for feeds).
This is because I don't see a point in organizing feeds hierarchically, and I think that you should be able to mix feeds together in multiple ways.
For example, I'd like to bundle [Simon Willison's Weblog](https://simonwillison.net) with other blogs, as well as with my tech news.
Maybe it's a worse system if you follow a thousand different high-frequency feeds but I don't.
I also decided to get rid of the sidebar and allow navigation solely through right-clicking and slash commands.
I've been using [Zen](https://zen-browser.app/) as my sole browser for about a year now and I really like that you can hide the side and navigation bars—screen space is precious on a 13-inch monitor!
The effect looks good on my reader as well.

I had a pretty good idea of how I wanted the interface to function and look but not the means to implement it myself, so I ended up using AI for that.
In fact, I had my agent go back and add some features that I hadn't thought of before (like OPML import and compliance with [these](https://rachelbythebay.com/frb/) guidelines) with minimal guidance.
There are some benefits to this approach: the process of writing the frontend was significantly expedited and it probably looks better than anything that I could have written myself on a reasonable timeframe.
Again, I don't think I would have made Celadon at all if the cost of making it weren't so low.
However, this use of "agentic engineering" comes at the cost of maintainability, performance, and creative control.
I've already caught the agent making some really dumb decisions about loading
{{< sidenote "data" >}}And only caught them because they were already causing latency issues on my toy database.{{< /sidenote >}}
so who knows what other problems I'll run into as I continue to use it.
The bright side is that if (when?) these AI tools get prohibitively expensive and something breaks, I'll be forced to _really_ understand the codebase.

{{< figure src="/ox-hugo/articles_full_screen.png" caption="<span class=\"figure-number\">Figure 1: </span>The main view of Celadon. As usual, I didn't get to reading most of this, but I didn't feel bad about it either." >}}

Furthermore, while I did choose the fonts, colors, and general layout of the app (unintentionally aping [Catfishing](https://catfishing.net/) in the process), many of the details were left to the agent to impute.
Button sizes, menu orderings, border weights, transition animations, and countless other little decisions all work together to define the impression that a UI makes.
However, since AI models  are trained to predict the most likely outcome over vast quantities of _existing_ data, they are not capable of doing anything interesting or unique within this domain.
Ted Chiang makes a general version of this [point](https://www.newyorker.com/culture/the-weekend-essay/why-ai-isnt-going-to-make-art) to argue that AI is incapable of making "good" art, and I think that it applies here to some degree as well.
On the other hand, UIs have to be functional, and part of that is using the design patterns that people have been trained to interact with since they started using electronic devices.
AI is great with typical!
The problem is that you still have to understand what constitutes a typical decision.
Don't quote me on this, but I'm pretty sure that a big part of good
{{< sidenote "design" >}}Or cooking, or filmmaking, or, arguably, making music.{{< /sidenote >}}
is that it knows when to innovate and when to stay familiar.
If I am using AI to fill in the details, then I am not enforcing such a distinction.

{{< figure src="/ox-hugo/celadon.svg" caption="<span class=\"figure-number\">Figure 2: </span>The logo, which I designed myself by the power of the branding class that I just took." >}}

Does the app suck, then?
I don't think so, because despite these (currently abstract) issues, it does what I want it to do.
I don't even know why I'm trying to justify it.
It works.
