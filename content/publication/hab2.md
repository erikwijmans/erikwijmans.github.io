+++
title = "Habitat 2.0: Training Home Assistants to Rearrange their Habitat"
date = 2021-06-30T11:13:40-04:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Andrew Szot", "Alex Clegg", "Eric Undersander", "**Erik Wijmans**", "Yili Zhao", "John Turner", "Noah Maestre", "Mustafa Mukadam", "Devendra Chaplot", "Oleksandr Maksymets", "Aaron Gokaslan", "Vladimir Vondrus", "Sameer Dharur", "Franziska Meier", "Wojciech Galuba", "Angel Chang", "Zsolt Kira", "Vladlen Koltun", "Jitendra Malik", "Manolis Savva", "Dhruv Batra"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = []

# Publication name and optional abbreviated version.
publication = "Neural Information Processing Systems (NeurIPS)"
acceptance = ""
conf_year = "2021"
oral = "top 3% of 9122 submissions"
awards = ""
publication_short = ""


# Abstract and optional shortened version.
abstract = "We introduce Habitat 2.0 (H2.0), a simulation platform for training virtual robots in interactive 3D environments and complex physics-enabled scenarios. We make comprehensive contributions to all levels of the embodied AI stack - data, simulation, and benchmark tasks. Specifically, we present: (i) ReplicaCAD: an artist-authored, annotated, reconfigurable 3D dataset of apartments (matching real spaces) with articulated objects (e.g. cabinets and drawers that can open/close); (ii) H2.0: a high-performance physics-enabled 3D simulator with speeds exceeding 25,000 simulation steps per second (850x real-time) on an 8-GPU node, representing 100x speed-ups over prior work; and, (iii) Home Assistant Benchmark (HAB): a suite of common tasks for assistive robots (tidy the house, prepare groceries, set the table) that test a range of mobile manipulation capabilities. These large-scale engineering contributions allow us to systematically compare deep reinforcement learning (RL) at scale and classical sense-plan-act (SPA) pipelines in long-horizon structured tasks, with an emphasis on generalization to new objects, receptacles, and layouts. We find that (1) flat RL policies struggle on HAB compared to hierarchical ones; (2) a hierarchy with independent skills suffers from 'hand-off problems', and (3) SPA pipelines are more brittle than RL policies."
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = "https://arxiv.org/abs/2106.14405"
url_preprint = ""
url_code = "https://aihabitat.org"
url_dataset = "https://aihabitat.org"
url_project = "https://aihabitat.org"
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""
press_coverage_tag = "Habitat 2.0"

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
image = "hab2-teaser.jpg"
caption = ""

+++
