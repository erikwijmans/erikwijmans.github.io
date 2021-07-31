+++
title = "Megaverse: Simulating Embodied Agents at One Million Experiences per Second"
date = 2021-06-30T11:13:16-04:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Aleksei Petrenko", "**Erik Wijmans**", "Brennan Shacklett", "Vladlen Koltun"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = [1]

# Publication name and optional abbreviated version.
publication = "International Conference on Machine Learning (ICML)"
acceptance = "1184 out of 5513 submissions = 21%"
conf_year = "2021"
oral = ""
awards = ""
publication_short = ""


# Abstract and optional shortened version.
abstract = "We present Megaverse, a new 3D simulation platform for reinforcement learning and embodied AI research. The efficient design of our engine enables physics-based simulation with high-dimensional egocentric observations at more than 1,000,000 actions per second on a single 8-GPU node. Megaverse is up to 70x faster than DeepMind Lab in fully-shaded 3D scenes with interactive objects. We achieve this high simulation performance by leveraging batched simulation, thereby taking full advantage of the massive parallelism of modern GPUs. We use Megaverse to build a new benchmark that consists of several single-agent and multi-agent tasks covering a variety of cognitive challenges. We evaluate model-free RL on this benchmark to provide baselines and facilitate future research."
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
url_pdf = "http://vladlen.info/papers/megaverse.pdf"
url_preprint = ""
url_code = "https://github.com/alex-petrenko/megaverse"
url_dataset = ""
url_project = "https://www.megaverse.info"
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""
press_coverage_tag = "Megaverse"

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
image = "megaverse-teaser.jpg"
caption = ""

+++
