+++
title = "DD-PPO: Learning Near-Perfect PointGoal Navigators from 2.5 Billion Frames"
date = 2019-09-26T16:03:24-04:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["**Erik Wijmans**", "Abhishek Kadian", "Ari Morcos, Stefan Lee, Irfan Essa, Devi Parikh, Manolis Savva, Dhruv Batra"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["1"]

# Publication name and optional abbreviated version.
publication = "International Conference on Learning Representations"
acceptance = "687 out of 2594 submissions = 26.5%"
conf_year = "2020"
publication_short = "ICLR"

# Abstract and optional shortened version.

abstract = "We present Decentralized Distributed Proximal Policy Optimization (DD-PPO), a method for distributed reinforcement learning in resource-intensive simulated environments. DD-PPO is distributed (uses multiple machines), decentralized (lacks a centralized server), and synchronous (no computation is ever 'stale'), making it conceptually simple and easy to implement. In our experiments on training virtual robots to navigate in Habitat-Sim, DD-PPO exhibits near-linear scaling -- achieving a speedup of 107x on 128 GPUs over a serial implementation. We leverage this scaling to train an agent for 2.5 Billion steps of experience (the equivalent of 80 years of human experience) -- over 6 months of GPU-time training in under 3 days of wall-clock time with 64 GPUs. <br/> This massive-scale training not only sets the state of art on Habitat Autonomous Navigation Challenge 2019, but essentially 'solves' the task -- near-perfect autonomous navigation in an unseen environment without access to a map, directly from an RGB-D camera and a GPS+Compass sensor.  Fortuitously, error vs computation exhibits a power-law-like distribution; thus, 90% of peak performance is obtained relatively early (at 100 million steps) and relatively cheaply (under 1 day with 8 GPUs). Finally, we show that the scene understanding and navigation policies learned can be transferred to other navigation tasks -- the analog of 'ImageNet pre-training + task-specific fine-tuning' for embodied AI. Our model outperforms ImageNet pre-trained CNNs on these transfer tasks and can serve as a universal resource (all models + code will be publicly available)."
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true
selected_groups = ["Large-scale Machine Learning"]

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = "https://arxiv.org/abs/1911.00357"
url_preprint = ""
url_code = "https://github.com/facebookresearch/habitat-api/tree/main/habitat-baselines/habitat_baselines/rl/ddppo"
url_dataset = ""
url_project = ""
url_slides = ""
url_video = "https://iclr.cc/virtual_2020/poster_H1gX8C4YPr.html"
url_poster = ""
url_source = ""
press_coverage_tag = "DD-PPO"

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does this page contain LaTeX math? (true/false)
math = false

# Does this page require source code highlighting? (true/false)
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "pointnav_fig_v2.png"
caption = ""

+++

# Introduction

We present Decentralized Distributed PPO (DD-PPO).  DD-PPO is synchronous and simple to implement.  We leverage DD-PPO to achieve
state of art results on the [Habitat Autonomous Navigation Challenge 2019](https://aihabitat.org/challenge/) and "solve" the task
of PointGoal Navigation for agents with RGB-D and GPS+Compass sensors.

Specifically, these agents
 almost always reach the goal (failing on 1/1000 val episodes on average), and
reach it _nearly as efficiently as possible_ -- nearly matching (within 3% of) the performance of a _shortest-path oracle_! 
It is worth stressing how uncompromising that comparison 
is -- in a _new_ environment, an agent navigating without a map traverses a path nearly matching the shortest path on the map. 
This means there is no scope for mistakes of any kind -- 
no wrong turn at a crossroad, 
no back-tracking from a dead-end, 
no exploration or deviation of any kind from the shortest-path. 
Our hypothesis is that the model learns to exploit the statistical regularities in the floor-plans of indoor environments (apartments, offices) in our datasets.

# Example Navigation Episodes

<iframe width="560" height="315" src="https://www.youtube.com/embed/wNDcvomBRt8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


This video shows the agent successfully navigating _22 meters_ across a house (the top down map is shown for visualization purposes only).  Notice the second right-hand turn the agent makes.
While walking through the kitchen, the agent is able to infer that given the distance it still needs to travel, the goal cannot be directly forward, and it is not likely to be toward the left
given that there is a wall.  Thus it correctly decides to go right and begins to turn such that it rounds the corner perfectly.


<iframe width="560" height="315" src="https://www.youtube.com/embed/a8AugVLSJ50" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


This demonstrates the agents ability to expertly backtrack once it is clear that it made the wrong decision.


# ICLR 2020 Presentation

The presentation of this work for ICLR 2020 can be found here [iclr.cc/virtual_2020/poster_H1gX8C4YPr](https://iclr.cc/virtual_2020/poster_H1gX8C4YPr.html)

