---
title: How to map IP to Geolocation in Wireshark
author: mohit
type: post
date: 2022-01-11T08:13:00+00:00
draft: true
url: /?p=2556
featured_image: http://www.mohitkr.com/wp-content/uploads/2022/01/nasa-Q1p7bh3SHj8-unsplash-scaled.jpg
categories:
  - Networking
tags:
  - Networking
  - Wireshark

---
<img decoding="async" loading="lazy" class="alignnone size-medium wp-image-2557" src="http://54.206.253.95/wp-content/uploads/2022/01/nasa-Q1p7bh3SHj8-unsplash-1.jpg" alt="" width="1" height="1" />

When you are analyzing the web traffic, you might come to a situation where you would have to analyze the traffic based on the their location of origin. We can map the traffic into Geolocation based on a feature available in Wireshark. In order to do so, we would require to download the database from [Maxmind.][1]

<iframe width=&#8221;560&#8243; height=&#8221;315&#8243; src=&#8221;https://www.youtube.com/embed/1scfydmxyFw&#8221; title=&#8221;YouTube video player&#8221; frameborder=&#8221;0&#8243; allow=&#8221;accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture&#8221; allowfullscreen></iframe>**<img decoding="async" loading="lazy" class="alignnone size-medium wp-image-2557" src="http://54.206.253.95/wp-content/uploads/2022/01/nasa-Q1p7bh3SHj8-unsplash-1.jpg" alt="" width="1" height="1" />**

You can follow along this video to configure your Wireshark to map IP address to Geolocation.

 [1]: https://dev.maxmind.com/geoip