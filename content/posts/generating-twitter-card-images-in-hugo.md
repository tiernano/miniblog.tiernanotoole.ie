---
title: Generating Titter Card Images in Hugo
date: 2022-10-13T00:38:53+01:00
tags: ['blogging', hugo']
---

So, I should have really gone to bed a couple hours ago, but instead I spent WAY TOO MUCH time figuring out how to get [Hugo](https://gohugo.io/) to generate a [Twitter Card image](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/summary-card-with-large-image), like below: 


{{< cloudinary "miniblog/blog-template_huf0c96828ae6a79ec8545d754b6353946_304030_filter_12397976358228456183.png" "400" >}}


Long story boring, the code is in my [miniblog repo](https://github.com/tiernano/miniblog.tiernanotoole.ie), but some important bits.

First, I made up an image template in [Photoshop](https://geni.us/1XQTu8) and put it into the [assets/opengraph](https://github.com/tiernano/miniblog.tiernanotoole.ie/tree/master/assets/opengraph) folder.

Next, I have the [following code](https://github.com/tiernano/miniblog.tiernanotoole.ie/blob/master/layouts/partials/opengraph/get-featured-image.html) used to generate the image. It is called by an [over-ridden twitter partial](https://github.com/tiernano/miniblog.tiernanotoole.ie/blob/master/layouts/partials/seo/twitter.html) which includes a link to the generated image. When all is said an done, Hugo builds that image using the info from the [get-featured-image.html](https://github.com/tiernano/miniblog.tiernanotoole.ie/blob/master/layouts/partials/opengraph/get-featured-image.html) file and writes it to disk.

It works, for now. I need to do some tweaks and make it look better, but my Photoshop skills are very lacking! More tweaks required!
