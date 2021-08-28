---
title: "Hello there!"
date: 2021-08-28T23:36:15+05:30
draft: true
---

Hello!
{{< rawhtml >}}
<img class="smol-logo" src="/img/logo.png" />
{{< /rawhtml >}}


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
