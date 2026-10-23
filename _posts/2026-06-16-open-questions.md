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

## Omission in AI Agent Security and Privacy

I've noticed that many problems in AI safety, security, and privacy can be boiled down to this idea of **omission**. An agent does something and tells the user that the task is complete, but that response can leave out important information about what happened along the way, especially related to security. Did the agent disclose private data? Did it modify something outside the task? Did it implement insecure code? The user sees the result, while much of the execution remains a black box.

Vibe coding is one example. Someone without security experience might ask an AI to build an application and receive working code with a SQL injection vulnerability. They may never know to look for it.

There seem to be at least two questions here: **what security requirements were never specified, and what security-relevant behavior was left out of the reported outcome?** A user may not know enough to state every requirement, and they might expect some requirements to be inherent. But even when a requirement is explicit, a completion message doesn't establish that the agent respected it. I think these fit under the same general umbrella, even if they need different approaches.

How can we make these omissions visible without expecting users to become security experts? What evidence would let us distinguish between a task being completed and its security requirements being satisfied? And how should an agent communicate what was checked and what remains unknown? I'm interested in this as a broader research direction, with individual projects addressing specific parts of the gap between what an agent reports and what its execution establishes.
