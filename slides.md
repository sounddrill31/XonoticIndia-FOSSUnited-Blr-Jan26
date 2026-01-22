---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false


# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 20min
---


<img style="vertical-align: top;" src="https://upload.wikimedia.org/wikipedia/commons/4/41/Xonotic_logo.svg"></img>

<a class="absolute bottom-8 left-0.3/2 -translate-x-1/2" href="https://www.wikidata.org/wiki/File:Xonotic_logo.svg"><sub>Image is licensed Under GPLv2</sub></a>
<div class="absolute bottom-8 left-1.8/2 -translate-x-1/2">

  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    <carbon:arrow-right class="inline"/>
  </span>
</div>

---
layout: 'two-cols'
---

<script setup>
import GameTimeline from './components/GameTimeline.vue'

const timelineData = [
  { 
    year: '1996', 
    title: 'Quake Engine Released', 
    description: 'id Software releases Quake engine source code under GPL.' 
  },
  { 
    year: '2005', 
    title: 'Nexuiz Releases', 
    description: 'Launched using Darkplaces Engine, heavily derived from Quake.' 
  },
  { 
    year: '2010', 
    title: 'Licensing Controversy', 
    description: 'Rights issues arise: Nexuiz name licensed for an unrelated PS3 game.' 
  },
  { 
    year: '2010 - Now', 
    title: 'Xonotic is Born', 
    description: 'Community forks the original code to create Xonotic (GPLv3+).' 
  },
]
</script>

::left::

# Xonotic

A fun, past paced, Open Source(GPLv3+) Arena First Person Shooter!

![Gameplay](https://media.infosec.exchange/infosec.exchange/media_attachments/files/115/894/876/092/041/746/original/81c92025ec1b6c83.jpg)


::right::

<div style="border-left:1px;height:2px"></div>

### Timeline of evolution

<GameTimeline :items="timelineData" />

<!-- 
Presenter Notes:


- 1996: id Software releases Quake and subsequently releases the source code for its engine under the GPL
- 2005: Nexuiz, a free and open-source arena first-person shooter game, is first released. It used the DarkPlaces engine, an advanced engine derived from the Quake engine, as its base.
- 2010: A controversy arises when the original developers of Nexuiz sell the rights to the name to Illfonic, who then developed and released a commercial version on Steam. The existing community, committed to a truly free and open-source project, decides to fork the game.
- 2010 to Now: The community fork begins development with the goal of improving the game and avoiding past mistakes, leading to the birth of the Xonotic project. 
  - <sub>The initial release of Xonotic is launched, carrying forward the spirit and gameplay of the original community-focused Nexuiz.</sub>


Focus: game screenshot

Introduction and engine used

Comparison to quake and unreal tournament

-->


---

# Player Statistics(Excluding Xonotic India)

<sub>Sourced from https://stats.xonotic.org on 16th Jan 2026</sub>

<div class="grid grid-cols-2 gap-4 mt-4">

<div class="text-center">
  <div class="text-xl font-bold mb-2">Since Oct 2011</div>
  <div class="text-sm opacity-70 mb-4">297,588 Players | 2.6M Games</div>
  
```mermaid
pie showData
    title All Time Games
    "DM" : 1122696
    "CTF" : 843379
    "CTS" : 228746
    "Duel" : 218317
    "CA" : 108080
    "Other" : 167939
```
</div>

<div class="text-center"> <div class="text-xl font-bold mb-2">Past 24 Hours(as of Jan 16 2026)</div> <div class="text-sm opacity-70 mb-4">371 Players | 475 Games</div>

```mermaid
pie showData
    title Last 24h Games
    "DM" : 303
    "CTS" : 69
    "CTF" : 54
    "CA" : 16
    "TDM" : 15
    "Other" : 18
```
</div>

</div>

<!-- 
Presenter Notes:
200k lifetime player count doesn't sound like much but this clearly shows the game is cared for by the community! 
-->

---
layout: 'two-cols-header'
---

# Situation in South/South-East Asia(as of 2022)

::left::
[From: Reddit in r/linux_gaming<br>
"Any xonotic players in South Asia?"](https://www.reddit.com/r/linux_gaming/comments/h032s7/any_xonotic_players_in_south_asia/)

There is clear demand! 

We see a small influx of users, especially every time people move to linux and discover it from their distribution's `Software Center`!

::right::
<img style="width: 85vw; " src="./assets/reddit-thread.png"></img>

<!--
Presenter Notes:
Costs nothing for me to run!

People in India are also generally more accepting of linux and the paradigm shift as students and devs quickly become power users, sometimes even adopting arch linux or nixOS. 

They tend to exploratorily try out various games that are recommended by their linux software centers.

Screenshot of users talking about setting up servers on reddit 
-->

---
layout: 'two-cols'
---

# Getting Started

- Step-1: Download it from https://xonotic.org/download
- Step-2: Extract the zip package
- Step-3: Run the executable

Alternatively, it can be found on:
- Flathub for Flatpak users only
- brew/Homebrew for MacOS users only

![Download screen](./assets/Download.png)

Supported by Windows, MacOS*, Linux Distros!

::right::

![mirrors list](./assets/Mirrors.png)

<!--
Presenter Notes:
Download Link QR codes(warning 1.2gb)
I will be running it from my distribution's package, sudo zypper install xonotic
-->


---

# AVOID THE MICROSOFT STORE VERSION, IT IS FAKE/Unofficial
last minute slide lol

<img style="width: 75vw; " src="./assets/unofficial.png"></img>

<!--
Presenter Notes:
Xonotic End by Samej_Play
-->


--- 
layout: 'two-cols-header'
---

# Game Mechanics(Video Guide)
Xonotic: A 10,000 ft Overview for Beginners (antibody)

<!--
Presenter Notes:
Overview video by antibody

Explains simple things like map guides, weapons, etc.
-->

<iframe src="https://www.youtube.com/embed/ev-rOXCzy_Y" title="Xonotic: A 10,000 ft Overview for Beginners" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

::right::

<img 
  src="https://api.qrserver.com/v1/create-qr-code/?size=250x250&data=https://www.youtube.com/watch?v=ev-rOXCzy_Y" 
  class="w-45 h-45 rounded-xl shadow-lg border border-gray-200 bg-white p-2"
/>

https://www.youtube.com/watch?v=ev-rOXCzy_Y

---
layout: 'two-cols-header'
---

# Xonotic India

<div class="grid grid-cols-2 gap-10 items-center">

  <div class="text-xl opacity-90 leading-relaxed">
    Xonotic India is a community server run by us! We also maintain game bridges and community chats on IRC, Telegram and Discord.
  </div>

  <div class="flex flex-col items-center justify-center">
    <img 
      src="https://api.qrserver.com/v1/create-qr-code/?size=250x250&data=https://india.xonotic.au" 
      class="w-45 h-45 rounded-xl shadow-lg border border-gray-200 bg-white p-2"
    />
    <a href="https://india.xonotic.au" class="mt-4 font-mono text-sm opacity-70 hover:opacity-100">
      india.xonotic.au
    </a>
  </div>

</div>

<script setup>
import HorizontalMetroTimeline from './components/HorizontalMetroTimeline.vue'

const xonoticTimeline = [
  { year: '2021-2022', title: 'Wanted Server' },
  { year: '2022', title: 'Got ARM64 OCI Free Tier' },
  { year: 'Feb 2023', title: 'Server Live' },
  { year: 'Mid 2023', title: 'Admin Inactive' },
  { year: 'Mid 2024', title: 'Systems Broke' },
  { year: 'Sep 2025+', title: 'Revival' },
]
</script>

<div class="mt-20">
  <HorizontalMetroTimeline :items="xonoticTimeline" />
</div>

<!--
Presenter Notes:

This had been a long time project for me, even back then. 
I was getting tired of high lag playing on Australian servers.

the server and what it's about
Introduction what why when

QR with website


Origin Work in progress timeline
-->

---
layout: 'two-cols-header'
---

# Current Setup

::left::
<img style="width: 85vw; " src="./assets/ServerArchitecture.png"></img>


::right::
<div style="border-left:1px;height:2px"></div>

Problems:
- Melanobot v1 is EOL/Unmaintained. 
  - The chat stops syncing every 10 or 14 days, need to restart server!
- Server doesn't scale past 25 or 50 concurrent players
- Lobby is dead most of the time(less than 3 concurrent players)
- Uses custom source-compiled darkplaces
  - Stat counter services see this as a "modified" server(stats.xonotic.org does not save our data)
- 0 Social Media Presence, not even SEO
- Runs at-cost, where the cost is 0. 
  - I do not get paid for this, I do not pay for this.

<!-- 
Presenter Notes:

Issues(considered "modified" since darkplaces is compiled from source and a few more things, chat relay dies every few days, not built to scale past 25-50 concurrent users)
-->

---
layout: 'two-cols'
---

# Why this? 
Why now? Why at all?

Why not?

<img style="width: 55vw; " src="./assets/pubg-0.png"></img>


::right::

"Xonotic Free FPS Game Jo Asia Ko Hila De Gi Pakistan & India Mein Viral ..."

"ASIA KA SASE TEZ FPS GAME  
***XONOTIC***  
PUBG SE BHI TEZ"

\- Mr,Sensor Truthturnament (2025)


<!--
Presenter Notes:
Saw one of videos these and got some motivation lol

I wanted to do right by the people who stumble upon this game and feel bad because servers are deadchat. 

Revival (PUBG/BGMI-esque video thumbnail shown, post-indiafoss motivation to go back to half abandoned things and work on them)

more funny screenshots in the next slide
-->

---

![img 1](./assets/pubg-1.png)
![img 2](./assets/pubg-2.png)
![img 3](./assets/pubg-3.png)


---
layout: 'two-cols-header'
---

# Thank you for attending!

Gameplay demo will begin soon, if we have time. 

::left::

<img 
  src="https://api.qrserver.com/v1/create-qr-code/?size=250x250&data=https://github.com/sounddrill31/XonoticIndia-FOSSUnited-Blr-Jan26" 
  class="w-45 h-45 rounded-xl shadow-lg border border-gray-200 bg-white p-2"
/>

https://github.com/sounddrill31/XonoticIndia-FOSSUnited-Blr-Jan26

https://india.xonotic.au/slides

::right::

# LLM Involvement
Presentation, Content and CFP is original, otherwise untouched by an LLM :)

AI Assisted:
- Website Code for https://india.xonotic.au
- Presentation: 
  - Vue Components(Timeline)
  - Diagram Formatting(Mermaid Pie Chart)
  - HTML scaffolding(Snippets Examples for images and more)

<!--
QR and URL to this presentation

Presenter Notes:
Time for Demo!!!
-->