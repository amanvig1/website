---
title: "Hello there!"
date: 2021-08-28T23:36:15+05:30
draft: true
summary: "Welcome to my blog"
slug: "first"
---

Hi!
{{< rawhtml >}}
<img class="smol-logo" src="/img/logo.png" />
{{< /rawhtml >}}


I'm Samyak Sarnayak. This post is mostly a placeholder to test [Hugo](https://gohugo.io/) and the [gruvhugo](https://gitlab.com/avron/gruvhugo) theme.

After porting over my old posts here, I have planned for a few more. Hopefully I will get to them soon.

The [about](/about) page will be the first one to be filled here, after this one of course.

{{< css.inline >}}
<style>
.smol-logo {
  height: 1em;
  position: relative;
  animation-duration: 1s;
  animation-name: slidedown;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
p {
  overflow: hidden;
}
@keyframes slidedown {
  from {
    top: 1.5em;
  }

  75% {
    top: 0.3em;
  }

  to {
    top: 0.2em;
  }
}
</style>
{{< /css.inline >}}
