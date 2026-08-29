---
layout: about
title: about
permalink: /

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

{% include author-profile.html %}

{% capture about_markdown %}
I am a first-year CS Ph.D. student at the University of Illinois Urbana Champaign (UIUC), advised by [Prof. Luyi Xing](https://www.xing-luyi.com/) and supported by the [UIUC Grainger SURGE Fellowship](https://grainger.illinois.edu/academics/graduate/funding/surge). My area of focus is in AI and systems security. Always open to collaboration on security-related projects!


Previously, I received my B.S. from NYU Shanghai, majoring in Computer Science and minoring in Cybersecurity and Data Science. During my time at NYU, I am honored to have worked with Prof. Hua Shen (NYUSH), Prof. Muhammad Shafique (NYUAD), and Prof. Xia Zhou (Columbia) on various security projects regarding coding LLMs and audio deepfakes.

{% endcapture %}
{{ about_markdown | markdownify }}
