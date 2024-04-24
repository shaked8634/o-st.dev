---
title: 'Working From a Hill'
date: 2024-04-23T14:55:00+01:00
tags: ["off-grid"]
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: true
description: "Desc Text."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true
disableShare: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
ShowCodeCopyButtons: true
cover:
    image: "static/images/wallpaper.jpg"
    alt: "Fancy wallpaper"
    caption: "If you read this I failed to find a suitable wallpaper which is sad"
    relative: false
    hidden: true
    responsiveImages: false
---


I recently had the opportunity to work from an off-grid farm somewhere in southern Portugal.

![Aeropress, if you read this I love you](/images/off-grid_farm.jpeg)

Waking up and going to sleep in nature is a wonderful experience which I can even 
recommend to the most city rats there are. However, it has the obvious drawback that 
you can't have the exact same life, and when your occupation heavily involves internet
usage, you can expect some friction. And by friction, I mean stable internet
connection 😮.

The owner has done its best to locate the antenna on a poll on the hill, but nature is 
unpredictable as it can be and there are ups and down and in the latency and bandwidth
throughout the day.

Though I do fantasize on a [Starlink](https://www.starlink.com/gb/roam) kit, I find it hard to justify the costs.

So I thought in this post to share some tools I used to overcome these limitations:

## Media downloaders
### Soundcloud-dl
Yes, I'll start with the "entertainment" though it might be an underestimation since I 
know many of us find it easier to concentrate and mitigate external disturbances by 
listening to music (or white noise for all you weirdos 😉).

So the first tool I propose is a simple tool to download soundcloud streams called
[soundcloud-dl](https://github.com/AYehia0/soundcloud-dl) and avoid the frequent stutter when the connection is unstable. 
This tool allows you to pass multiple links to tracks or sets and reliably download 
them for hours of listening joy.

### yt-dlp
Whether you download videos for entertainment or education, YouTube is extremely sensitive
to network interference. And the advertisements in the middle get a different type of 
annoyance since they stop the stream download which causes further delay. The legendary
[yt-dlp]() comes to save the day. This tool also gets multiple links and also supports
controlling the downloaded audio and video quality. After few tries the only syntax I'm 
using is to choose a smaller size:
```shell
yt-dlp -S +size 'https://www.youtube.com/watch?v=dQw4w9WgXcQ' 'https://www.youtube.com/watch?v=1_Z5q152GSQ'
```

## Web
### Lynx
For anyone that isn't familiar with [Lynx](https://lynx.invisible-island.net/) it's a CLI browser with a tiny number of dependencies. The web experience
lets say it requires getting used to, and IMHO the speed gained over a modern browser is debatable. So why I'm bothering
mentioning it here? Because in some cases like searching for something. It's very convenient to browse results from the
CLI since it's fast rendering only text and the memory footprint is neglectable. 

## RSS
I rediscovered RSS a while ago when I started participating more in forum discussions 
and found how useful it is to scour interesting posts instead of browsing each forum
separately.
I still didn't find a good solution to synchronize the feeds I'm following across my 
phone where I'm using the awesome [feeder](https://duckduckgo.com/?q=android+feeder+rss&ia=web)
and on my desktop I'm using the  

## AI
For AI, I can either rely on the internet connection or be patient and wait for the
generated text to appear using  local model:

### ChatGPT
OpenAI WEB UI and API seems to handle unstable internet connection just fine, so I'm just using 
it normally either from the Web UI or with [Continue plugin](https://github.com/continuedev/continue)

### Ollama
I also run local LLM (though my humble laptop can barely run 7b GGUF models) with [ollama](https://github.com/ollama/ollama) 
and use [oterm](https://github.com/ggozad/oterm) to communicate. 

## Bonus
### Gemini
If you manage to hold until here, and you find you have time to spare since the 
internet is sloowww then you can discover with me the new web protocol with vintage scent
[Gemini](https://geminiprotocol.net/).

---

Thanks for reading so far. If you like or dislike something feel free to comment and
add your suggestion. This 