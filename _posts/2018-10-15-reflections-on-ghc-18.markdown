---
title: "Reflections on Grace Hopper Celebration 2018"
layout: post
date: 2018-10-15 15:00:00 -0400
image: /assets/images/markdown.jpg
headerImage: false
tag:
category: blog
author: cherylbrown
description: Reflections on Grace Hopper Celebration 2018
# jemoji: '<img class="emoji" title=":ramen:" alt=":ramen:" src="https://assets.github.com/images/icons/emoji/unicode/1f35c.png" height="20" width="20" align="absmiddle">'
---

A couple of weeks ago, I went to the [Grace Hopper Celebration](https://ghc.anitab.org/) (GHC), which is the world's largest gathering of women in computing with over 20,000 total attendance. This year, the conference was held at the George R. Brown convention center in Houston, Texas from September 25th - 28th. I was part of a group of about 180 women from IBM who were invited to attend.

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-we-are-here.jpg" />
</div>

The opening and closing keynotes were held at the Toyota Center in Houston, and it was packed to the brim for both sessions. When you are used to being the only woman in your Comp Sci class or the only woman on your development team, it is really amazing to be in an arena with 20,000 other technical women. That alone was very energizing and inspiring, and helps keep the impostor syndrome we often feel at bay.

There were also hundreds of breakout sessions over the course of the conference covering topics ranging from technical and career related to personal and, at times, politically related topics. I will share the highlights of each session I attended below. From a technical perspective, I most enjoyed a session on DevOps and site reliability engineering called *"When 99.9% Isn't Good Enough"* and another session called *"Demystifying Performance Analysis"* on how to best measure, maintain, and improve site performance. There were some good takeaways from those that I think we could possibly implement on our IBM Marketplace services.

From a personal perspective, and by far the top highlight of the conference for me, I very much enjoyed a session with Anita Hill on *"The Past, Present, and Future of the #MeToo Movement"*. Anita Hill's session had been planned for some time, but it so happened that during the conference, the U.S. Senate was in the midst of hearings regarding the nomination of Judge Brett Kavanaugh to the Supreme Court, and the sexual abuse allegations made against him by Dr. Christine Blasey Ford. It felt in some ways like a weird replay of events from 20 years earlier, and a gnawing reminder of just how little progress women have made, despite being at this conference that was supposed to be empowering and motivating women to break further into an industry heavily dominated by men, especially in its upper ranks.

That being said, Anita Hill's message left me inspired not to give up. She reminded us to take a moment when we feel defeated, but then to ask ourselves, "What are you going to do about it?" and to keep going. She said to keep the long term goal in mind, and it reminded me that progress is not always a straightforward path. Sometimes it may come in fits and starts, sometimes it may seem like things are going backwards or around in loops, but on the whole we have to keep pushing forward. She also encouraged us to reach out to younger women and our alma maters or local universities and ask not only how we can help, but what we can learn from them. Since then, I have decided to become a mentor in the IBM/North Carolina State University PathFinder program, and will begin a mentoring relationship with a young woman in Computer Science this fall. I am looking forward to finding other ways to give back, and be an advocate and example for other technical women in the workplace.

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-ibm-team.jpg" />
</div>

---

# Individual Session Details

Each session I attended at the conference is listed below, as well as a few key takeaways from each session.

# Day 1

## Opening Keynote

### Padmasree Warrior, CEO, NIO

- Pay attention to how the tech industry is changing. For example, the car as a platform is coming in the future
- Take positions where 70% of the time you know what you're doing, and 30% you will learn as you go
- When you're doing well in your career, it time to look for your next opportunity

### Jessica Matthews, CEO, Uncharted Power

- Founded Uncharted Power to help the 1 billion people around the world who don't have electricity using day-to-day items like the Soccket and the Pulse
- "Just because it's not your plan, doesn't mean it's not your destiny."
- "Being underestimated was the best thing that has ever happened to me." I can relate to this!

## Money is Power

**Panel on personal finance with Christine Benz (Morningstar), Kristy Wallace (Elevate/Elevest), Lauri Hofherr (Oranj), Meg Bartelt (Flow Financial Planning), Alison Heisner (Personal Capital)**

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-money-is-power.jpg" />
</div>

- Money give you power, flexibility, and choice
- 27% of working women are not offered 401k by employers, compared with 14% of men
- 40% of women haven't invested in their retirement plans, compared with 33% of men
- Proper amount of company stock to have is zero. It's better to be diversified.
- It seems obvious, but you need to understand what you're investing in before you invest in it

## Think Like a Hacker

**Workshop by Kranthi Daruapu, Greg Fukushima, Crystal Ro (all from Morgan Stanley)**

- It's everyone's responsibility to think about cyber security
- Attacks are composed of reconnaissance, initial access, persistence, getting to the target, and executing the attack
- To defend against recon, research your public footprint, limit details of job roles in public especially for sysadmins and security roles (e.g. your tech stack), minimize exposure of infrastructure
- To defend against persistence, standardize your builds, control private access, restrict access to network resources, monitor for scanning behavior
- To defend against initial access, keep software patched, use 2-factor auth, deploy endpoint detection and response, understand network, whitelist IPs of vendors
- To defend the target, segment the network, control access entitlements based on job role, monitor network activity for abnormalities
- To defect against an attack, know your network, segment the network and have layered defenses in place, organize data, actively seek out threats, develop relationships between security response and ops teams

## Microservices, Serverless, Real Time Data Pipelines

**Short talk given by Manisha Sule**

- Advantages of microservices: You build it you own it, break down a monolithic problem, develop in parallel, allows Agile, diverse tech stacks are possible, better failure detection, enhanced CI/CD, autonomy and ownership all the way to production
- Disadvantages: Can be cumbersome if number of microservices gets into the hundreds or more, DevOps is a must, possibility of code duplication increases, change in a communication contract can affect several services
- Advantages of serverless: Infrastructure is managed by the cloud provider, fully managed, highly available, scalable, no provisioning, zero administration
- Disadvantages: Vendor lock in, lack of visibility, not for stateful applications, limited by timeout

## When 99.9% Isn't Good Enough

**Panel on site reliability engineering and DevOps with Jennifer Petoff (Google), Leslie Carr (Quip), Emily Burns (Netflix), Anne Cesa Klein (Pure Storage)**

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-sre-and-devops.jpg" />
</div>

- 100% uptime is an impossible goal to achieve
- You error budget = 100% - your uptime goal. e.g. 100% - 99.9999% = 0.001% or less than one hour per year. This is the ammount of time you have to innovate. Once your uptime drops below your SLO, it's time to focus on technical debt.
- Blameless postmortems are essential to improve reliability because blameful tends to cause cover ups
- Try to degrade your service's performance before going down (e.g. video quality degradation on Netflix)
- Waking up in the middle of the night to answer a page is old school, you should have services that can heal themselves
- After a deployment, redirect some % of the traffic to the new deployment and test before going 100% live
- Never be afraid to fail, but never fail the same way twice

---

# Day 2

## Engineering Change at Scale

**Talk by Priscilla Chan (Chan Zuckerberg Initiative)**

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-chan.jpg" />
</div>

- It's up to you to fix the big problems in the world
- Choose to tackle the messy or ambiguous problems
- Ask yourself, if you're not going to do it, who is?
- Find out what makes you passionate, what gets you out of bed in the morning, and what makes you want to solve a hard problem

## Running Metadata Storage at Petabyte Scale

**Short talk by Olga Kechina (Dropbox)**

- Dropbox was born on MySQL but became a maintenance hassle and could not scale
- Dropbox built a layer on top of MySQL called Edgestore which dealt with objects and their relationships, and automatically took care of scaling, partitioning, etc.
- However, 10s of petabytes became very expensive in terms of hardware with this model and not everyone needs the graph API provided by Edgestore
- Currently solving this problem by creating a simpler API and replacing he underlying data store

## Demystifying Performance Analysis

**Talk given by Ariane Jansen (Facebook)**

- You can't improve what you can't measure
- Measure locally, in a lab, and in the wild - instrument all environments in the same way
- Aggregate day to day trends and keep long term trend lines
- Once you know your key drivers, alert on them
- If you understand your current performance, have fast turnaround when there are regressions, and stop regressions from shipping you are doing well

## Miscellaneous

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-expo.jpg" />
</div>

- On Day 2, I spent some time at the Expo where hundreds of companies from Google and Amazon, to Stubhub and Retailmenot where recruiting. It was awesome and overwhelming!
- I also went to two AWS workshops, one on building an Alexa skill and one on building a website with Route 53, S3, Cloudfront, API Gateway, Lambda, and DynamoDB
- On Wednesday evening, IBMers were invited to enjoy drinks and appetizers with the 180 women from IBM at a local Italian restaurant called Damian's

---

# Day 3

## The Past, Present, and Future of the #MeToo Movement

**Moderated Q&A session with Anita Hill**

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-anita-hill.jpg" />
</div>

- Sexual harassment survivors feel a sense of isolation after watching Dr. Ford's testimony, #MeToo is about making everyone feel less isolated
- Dr. Ford told her story when she needed to and when her country needed her to
- Women still have a long way to go to be able to have the kind of power and anger that Judge Kavanaugh displayed during his testimony
- Not sure legislation will fill the lack of rights for women, but private companies can. Duke's commitment to diversity and inclusion and Tim Ryan (Pwc) corporate diversity pledge were mentioned as examples.
- The work we are doing for inclusion is an honor, worthy of our talent and energy
- When you try to change culture, there is resistance, but stay in there, work with others, recognize small triumphs, and remember that women in the world need you
- Tap back into you alma maters and find out what the women there need from you, and what you can learn from them
- When you feel like giving up, take a break but do not retreat. Ask yourself what are you going to do? How are you going to respond?

## How to Break Into Conference Speaking

**Talk given by Diana Yuo (Facebook) and Charu Jangid (LinkedIn)**

- Understand your sweet spot topic
- Look at speakers you admire and what they speak about
- Find what you feel passionate about, and develop a personal brand around it
- Speak at company events, find your company's annual summits, and meet the organizers of those events
- If rejected when applying to give a talk, ask what you can improve for next time

## Launching Our Future

**Talk given by Gwynne Shotwell (SpaceX)**

<div style="display:table-cell; vertical-align:middle; text-align:center">
  <img style="width: 50%" src="/assets/images/ghc18-gwynne-shotwell.jpg" />
</div>

- Driving principles of SpaceX are absurdly ambitious goals, rapid innovation, continuous feedback, and an exceptional team
- Strong belief that diversity shouldn't even be a thing, it should just be fact

## Closing Keynote

- Dr. Justine Cassell (Carnegie Mellon) spoke about the AI work she is doing and how to use AI in a positive way
- Holly Liu (Kabam founder) won the Technology Entrepreneurship Abie Award and emphasized that you shouldn't wait to do the things you aspire to
- [Times Up Tech](https://TimesUp.Tech) was announced, a spin of group from the Times Up movement, specifically geared towards the tech industry
- Brenda D'Arden (sp?) reminded us that if we lose ANY of our community members due to lack of support we are not doing our job

<div style="display:table-cell; vertical-align:middle; text-align:center; padding-bottom: 50px">
  <img style="width: 50%" src="/assets/images/ghc18-closing-keynote.jpg" />
</div>
