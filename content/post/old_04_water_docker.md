---
title: "On water and systems"
date: 2021-07-04
tags:
  - 1,000 foot view
draft: false
summary: "or how docker is a plumbing system"
aliases:
 - "/blog/tech/water-docker/"
slug: "water-docker"
---

There's a lake a few hundred meters from your house, with plenty of water in it. Can you actually use the water though? Sure, you can take a bucket to the lake, fill it up, bring it back and use it. You'll need more than a bucket of water, so you make multiple trips and take two buckets at a time. Now you're spending quite a bit of your time and energy everyday in this. To make your life easier, you build a rudimentary plumbing system. You take a long enough pipe, connect a motor and that's it, you now have easy access to water. You can use this, but what about your neighbour, your colony? Everyone will need to build their own pipelines, which isn't sustainable as every one of them needs to do all of the maintenance themselves, costing a lot of time and resources. You would need a real plumbing system that has robust pipes, a temporary storage (a tank), a better motor and you would have to rethink your home's architecture to stuff all the pipes in there. Only then do you get water at your tap.

My point is that you could say that the water is right there but it's not actually useful without all the plumbing around it. With the plumbing it's a lot more convenient to do the things you do with water as you have it right at your tap, anytime you need it.


---

I realized this when I was brushing my teeth one morning. The day before, I was working on [making my own container runtime](https://github.com/Samyak2/guntainer) to learn how containers work. I made a connection between this water story and containers.
Namespaces and cgroups in Linux together let you isolate a process and limit the amount of resources it can use. That is basically what containers do, but to use them you need to jump through lots of hoops. My container runtime is that rudimentary pipeline that works but isn't sustainable and cannot be (or will not be) used by anyone other than me. To make this useful you would need an entire system that is maintained by a group of people who know what they are doing - like [Docker](https://www.docker.com/).

---

Whenever there's a discussion of using Linux over Windows/MacOS, one argument that often comes up is that Linux allows you to do basically anything you want to and if you miss a feature from Windows/MacOS you can implement it yourself or use a community made alternative (if it exists). Again, the difference between something being possible and actually usable is bigger than what AWS Infinidash will be in a few months (trust me it's going to huge :)).
One example of this is MacOS' Time Machine - the snapshot tool. On Linux, [Btrfs](https://btrfs.wiki.kernel.org/index.php/Main_Page) supports snapshots but to use it you need an app that makes managing snapshots easier ([snapper](http://snapper.io/) is one).

---

Those were my thoughts. I realize that this is quite obvious in hindsight, but I wanted to share this anyway. Have you noticed this pattern somewhere else? Let me know down below or reach out to me on any of the links to the left.

Thank you for reading. Bye!
