+++
title = "Auxiliary Tasks Speed Up Learning PointGoal Navigation"
date = 2020-07-09T20:50:26-04:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Joel Ye", "Dhruv Batra", "**Erik Wijmans**&ast;", "Abhishek Das&ast;"]

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
publication = "arXiv"
acceptance = ""
conf_year = ""
oral = ""
awards = ""
publication_short = ""


# Abstract and optional shortened version.
abstract = "PointGoal Navigation is an embodied task that requires agents to navigate to a specified point in an unseen environment. Wijmans et al. showed that this task is solvable but their method is computationally prohibitive, requiring 2.5 billion frames and 180 GPU-days. In this work, we develop a method to significantly increase sample and time efficiency in learning PointNav using self-supervised auxiliary tasks (e.g. predicting the action taken between two egocentric observations, predicting the distance between two observations from a trajectory,etc.).We find that naively combining multiple auxiliary tasks improves sample efficiency,but only provides marginal gains beyond a point. To overcome this, we use attention to combine representations learnt from individual auxiliary tasks. Our best agent is 5x faster to reach the performance of the previous state-of-the-art, DD-PPO, at 40M frames, and improves on DD-PPO's performance at40M frames by 0.16 SPL."
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
url_pdf = "https://arxiv.org/abs/2007.04561"
url_preprint = ""
url_code = "https://github.com/joel99/habitat-pointnav-aux"
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""
press_coverage_tag = ""

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
image = "habitat-memory-aux-teaser.jpg"
caption = ""

+++
