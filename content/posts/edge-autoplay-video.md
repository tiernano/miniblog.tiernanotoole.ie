---
title: turning off Edge Autoplay Video
date: 2022-09-12T19:55:00+00:00
tags: ["edge", "tips_and_tricks", "browsers"]
---

After moving to Edge from Firefox a few days back, i noticed all the stupid autoplay videos are back... After a bit of digging, there are a couple of steps to fix this:

First, go to [edge://flags](edge://flags). Search for **Show block option in autoplay settings** and mark it **Enabled**

{{< cloudinary "miniblog/image-20220912205725302.png" "400">}}

Restart your browser and now to go [edge://settings/content/mediaAutoplay](edge://settings/content/mediaAutoplay)

Select Block. This will block all Autoplaying Video on all sites. If you want to enable a particular site, you can add it to the allow list.

{{< cloudinary "miniblog/image-20220912205850661.png" "400">}}

And that's it! No more stupid autoplaying videos!
