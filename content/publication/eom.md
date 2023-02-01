+++
title = "Emergence of Maps in the Memories of Blind Navigation Agents"
date = 2023-01-22T12:10:17-05:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["**Erik Wijmans**", "Manolis Savva", "Irfan Essa", "Stefan Lee", "Ari Morcos", "Dhruv Batra"]

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
acceptance = "" #"1558 out of 4900 submissions = 31.8%"
conf_year = "2023"
extra = "Notable Top 25%, 389 out of 4900 submissions = top-8%"
awards = ""
publication_short = "ICLR"


# Abstract and optional shortened version.
abstract = ""
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true
selected_groups = ["Characterizing Emergent Intelligence"]

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = "http://arxiv.org/abs/2301.13261"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = "/publication/eom"
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""
press_coverage_tag = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does this page contain LaTeX math? (true/false)
math = true

# Does this page require source code highlighting? (true/false)
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = "eom-teaser.jpg"
caption = ""

+++

# Introduction

Decades of research into intelligent animal navigation posits that organisms build and maintain inter-
nal spatial representations (or maps) of their environment, that enables the organism to determine
and follow task-appropriate paths.
Hamsters, wolves, chimpanzees, and bats leverage prior exploration to determine and follow short-
cuts they may never have taken before.  Even blind mole rats and animals rendered situationally-blind in dark environments demonstrate shortcut behaviors. Ants forage for food along meandering paths but take near-optimal
return trips, though there is some controversy about whether insects like
ants and bees are capable of forming maps. 

Analogously, mapping and localization techniques have long played a central role in enabling non-
biological navigation agents (or robots) to exhibit intelligent behavior.
More recently, the machine learning community has produced a surprising phenomenon – neural-network models for navigation that curiously
do not contain any explicit mapping modules but still achieve remarkably high performance For instance, Wijmans et al. (2020) showed that
a simple ‘pixels-to-actions’ architecture (using a CNN and RNN) can navigate to a given point in
a novel environment with near-perfect accuracy; Partsey et al. (2022) further generalized this result
to more realistic sensors and actuators. Reed et al. (2022) showed a similar general purpose architecture (a transformer) can perform a wide variety of embodied tasks, including navigation. The
mechanisms explaining this ability remain unknown. Understanding them is both of scientific and
practical importance due to safety considerations involved with deploying such systems.

In this work, we investigate the following question – is mapping an emergent phenomenon? Specifically, do artificial intelligence (AI) agents learn to build internal spatial representations (or ‘mental’
maps) of their environment as a natural consequence of learning to navigate?

# Task

The specific task we study is PointGoal navigation, where an AI agent is
introduced into a new (unexplored) environment and tasked with navigating to a relative location –
'_go 5m north, 2m west relative to start_'. This is analogous to the direction and distance of foraging
locations communicated by the waggle dance of honey bees. 

# Agent input and design

Unlike animal navigation studies, experiments with AI agents allow us to precisely isolate map-
ping from alternative mechanisms proposed for animal navigation – the use of visual land-
marks orientation by the arrangement of stars, gradients of
olfaction or other senses. We achieve this isolation by judiciously designing
the agent’s perceptual system and the learning paradigm such that these alternative mechanisms are
rendered implausible. Our agents are effectively ‘blind’; they possess a minimal perceptual system
capable of sensing only egomotion, i.e. change in the agent’s location and orientation as the it moves
– no vision, no audio, no olfactory, no haptic, no magnetic, or any other sensing of any kind. This
perceptual system is deliberately impoverished to isolate the contribution of memory, and is inspired
by blind mole rats, who perform localization via path integration and use the Earth’s magnetic field
as a compass. Further still, our agents are composed of navigation-agnostic,
generic, and ubiquitous architectural components (fully-connected layers and LSTM-based recurrent neural networks), and our experimental setup provides no inductive bias towards mapping – no
map-like or spatial structural components in the agent, no mapping supervision, no auxiliary tasks,
nothing other than a reward for making progress towards a goal.


# Results

Surprisingly, even under these deliberately harsh conditions, we find the emergence of map-like
spatial representations in the agent’s non-spatial unstructured memory, enabling it to not only successfully navigate to the goal but also exhibit intelligent behavior (like taking shortcuts, following
walls, detecting collisions) similar to aforementioned animal studies, and predict free-space in the
environment. Essentially, we demonstrate an ‘existence proof’ or an ontogenetic developmental ac-
count for the emergence of mapping without any previous predisposition. Our results also explain
the aforementioned surprising finding in recent literature – that ostensibly map-free neural-network
achieve strong autonomous navigation performance – by demonstrating that these ‘map-free’ systems in fact learn to construct and maintain map-like representations of their environment.

Concretely, we ask and answer following questions:

## Is it possible to effectively navigate with just egomotion sensing? 


Yes. We find that our ‘blind’
agents are highly effective in navigating new environments – reaching the goal with 95.1%$\pm$1.3%
success rate. And they traverse moderately efficient (though far from optimal) paths, reaching
62.9%$\pm$1.6% of optimal path efficiency. We stress that these are novel testing environments, the
agent has not memorized paths within a training environment but has learned efficient navigation
strategies that generalize to novel environments, such as emergent wall-following behavior.


## What mechanism explains this strong performance by ‘blind’ agents? 


<img src="/files/eom-post/perf-vs-mem-len-post-hoc.jpg" alt="Blind Agent Performance" width="50%"/>


Memory. 
We find that
memoryless agents completely fail at this task, achieving nearly 0% success. More importantly,
we find that agents with memory utilize information stored over a long temporal and spatial horizon and that collision-detection neurons emerge within this memory. Navigation performance as
a function of the number of past actions/observations encoded in the agent’s memory does not saturate till one thousand steps (corresponding to the agent traversing 89.1$\pm$0.66 meters), suggest-
ing that the agent ‘remembers’ a long history of the episode.

The video bellow shows a video of a blind agent navigating (right) and the t-SNE projection of the portion of it's hidden state responsible for 
detecting collision. The black dot is where the agent's hidden state is for the current state. Notice that the hidden state stays within the same
cluster throughout a series of actions.

<video height="100%" width="100%" controls autoplay>
<source src="/files/eom-post/collision-neuron-vis.mp4" type="video/mp4">
</video>

## What information does the memory encode about the environment? 

![Decoded Occupancy Maps](/files/eom-post/occupancy-map-figure-good-only.jpg)

Implicit maps. We perform
an AI rendition of Menzel (1973)’s experiments, where a chimpanzee is carried by a human and
shown the location of food hidden in the environment. When the animal is set free to collect the
food, it does not retrace the demonstrator’s steps but takes shortcuts to collect the food faster.
Analogously, we train a blind agent to navigate from a source location (S) to a target location
(T). After it has finished navigating, we transplant its constructed episodic memory into a second
‘probe’-agent (which is also blind). We find that this implanted-memory probe-agent performs
dramatically better in navigating from S to T (and T to S) than it would without the memory
transplant. Similar to the chimpanzee, the probe agent takes shortcuts, typically cutting out
backtracks or excursions that the memory-creator had undertaken as it tried to work its way
around the obstacles. These experiments provide compelling evidence that blind agents learn to
build and use implicit map-like representations of their environment solely through learning to
navigate. Intriguingly further still, we find that surprisingly detailed metric occupancy maps of
the environment (indicating free-space) can be explicitly decoded from the agent’s memory.

This videos show a blind agent navigating from source to target and then a probe navigating from target to source.
Notice the increase efficiency and reduction in collisions of the probe during the return trip.

<video height="100%" width="100%" controls autoplay>
<source src="/files/eom-post/probe-example.mp4" type="video/mp4">
</video>

## Are maps task-dependent? 


<img src="/files/eom-post/excursion-forgetting.jpg" alt="Excursion Forgetting" width="75%"/>

Yes. We find that the emergent maps are a function of the navigation
goal. Agents 'forget' excursions and detours, _i.e._ their episodic memory only preserves the
features of the environment relevant to navigating to their goal. This, in part, explains why
transplanting episodic memory from one agent to another leads it to take shortcuts – because the
excursion and detours are simply forgotten.


# Conclusion

Overall, our experiments and analyses demonstrate that ‘blind’ agents solve PointGoalNav by
combining information over long time horizons to build detailed maps of their environment, solely
through the learning signals imposed by goal-driven navigation. In biological systems, convergent
evolution of analogous structures that cannot be attributed to a common ancestor (_e.g._ eyes in
vertebrates and jellyfish) is often an indicator that the structure is a natural
response to the ecological niche and selection pressures. Analogously, our results suggest that
mapping may be a natural solution to the problem of navigation by intelligent embodied agents,
whether they be biological or artificial. We now describe our findings for each question in detail.