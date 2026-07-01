---
layout: post
title: Things I've Thought About
date: 2026-06-30 22:33:00
description: Questions I've pondered without answers.
tags: research
categories: 
---
These are some questions research topics I've formulated but haven't found a point I've been stuck at. I'd love to collaborate on any of these topics and get any advice!  

## LLM Alignment using Policy Debate
In high school, I had a brief stint in [policy debate](https://en.wikipedia.org/wiki/Policy_debate). Although my time as an active debater was short, the activity changed my life in ways I could never imagine. Policy debate was a rigorous testing environment for argumentation, a space where arguments were methodologically broken down and critiqued. 

I believe this can be used to evaluate LLM capability on strong argumentation tasks. To my knowledge, there doesn't exist a high quality, large-scale dataset that can be evaluated against a human ground truth. A couple reasons why policy debate is a good candidate for argumentative tasks include: a corpus of **policy debate rounds**, a human judge who has a **paradigm** (how a judge will evaluate a debate round), and the **reason for decision** (why the judge voted the way they did). Existing works [[1]](https://arxiv.org/abs/2406.17169)[[2]](https://aclanthology.org/2025.findings-emnlp.926/) mainly consider small logical reasoning tasks, similar to riddles, but not so much as to considering weighing different arguments against each other.

However, I've run into some similar limitations. Audio quality from debate round recordings are not the best. Policy debaters speak really fast and microphones are typically placed far away from them. This isn't an issue for trained ears but speech-to-text models lack capabilities in transcribing rounds. 

You can check out the project [here](https://github.com/ash-jyc/db84llm.git).