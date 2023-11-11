---
authors: waka
title: "Video Playback Improvement"
tags: [Blog Post]
---

ArchivD -as my first SaaS product- has been running for about a month, and during this short period of time I collected data from several activities that occurred. This data may be less than valid because it was collected over a short period of time, however this is still stands as an improvement that can allow you to enjoy ArchivD even more than before.

<!--truncate-->

## The datas and verdict

So over the past month I have seen a quite significant increase in usage. In the first month, ArchivD was trusted to stored at least 2.220 files with a total of 265 GB of files, at least. Even though it's not a fantastic number for the other, but for me this is something very extraordinary. I mean come on, this project is finally starting to show results. I couldn't be happier than this.

Ok, so back to our topic about statistics from the data I have collected over the past month. One of the interesting things is, perhaps because ArchivD offers a video player feature, this causes the ratio of video playbacks to be higher than downloads. To be honest, really high. Regardless, it's gotten to the point where bandwidth billing looks quite worrying.

Uh ohh... To be honest, I didn't anticipate this at first. I mean from the start what I envisioned was that ArchivD would focus on download-driven rather than video playback.

So I'm pretty sure that the video playbacks experience by the most of users over the past month has been quite poor. You see, i set that the video link will expire and cannot be used within 1 hour for users who are not logged in, or 3 hours for free users. All thanks to token-based links.

Therefore to enhance the experience in the last few days I have looked for and implemented several alternatives so that video playback can be done without time limitations due to the tokens. Several implementations ended in failure and did not go as desired, but the latest implementation was successful (and it has been implemented).

I won't talk about boring technical issues like how-to, but the verdict is that now video playback will not run based on tokens request, so that video playback will always be available 24/7 whenever you click that play button.

Apart from that, now every video playback has a cache applied by default to make playback even smoother.

Cheers!