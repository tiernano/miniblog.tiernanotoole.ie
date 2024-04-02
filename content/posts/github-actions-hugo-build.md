---
date: 2024-04-01T19:45:00Z
title: "Building and Deploying Hugo Apps using GitHub Actions to Cloudflare Pages"
tags: ["tutorial"]

---
It's been a while since I did anything with this site, but today I have modified the way it deploys. It used to deploy directly using [Cloudflare Pages](https://pages.cloudflare.com/) and [Cloudflare](https://cloudflare.com) did the building of the Hugo site and then deployed the result. Today, I swapped it to use [GitHub Actions](https://github.com/features/actions). This allows me to do other fun stuff after the build is finished. For example, I can run tools like [Jampack](https://jampack.divriots.com/) to compress the site and images before deploying to CLoudflare Pages. I could also run something like [Markdownlint](https://github.com/igorshubovych/markdownlint-cli) before building the Hugo site, but that's a future job...

The Workflow for the site is [up on Github](https://github.com/tiernano/miniblog.tiernanotoole.ie/blob/master/.github/workflows/main.yml). I will be making tweaks to this over time.
