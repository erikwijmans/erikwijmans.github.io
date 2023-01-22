+++
title = "How to Train PointGoal Navigation Agents on a (Sample and Compute) Budget"
date = 2020-12-14T11:14:39-05:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["**Erik Wijmans**", "Irfan Essa", "Dhruv Batra"]

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
publication = "International Conference on Autonomous Agents and Multiagent Systems (AAMAS)"
acceptance = ""
conf_year = "2022"
extra =""
awards = ""
publication_short = ""


# Abstract and optional shortened version.
abstract = "PointGoal navigation has seen significant recent interest and progress, spurred on by the Habitat platform and associated challenge. In this paper, we study PointGoal navigation under both a sample budget (75 million frames) and a compute budget (1 GPU for 1 day). We conduct an extensive set of experiments, cumulatively totaling over 50,000 GPU-hours, that let us identify and discuss a number of ostensibly minor but significant design choices -- the advantage estimation procedure (a key component in training), visual encoder architecture, and a seemingly minor hyper-parameter change. Overall, these design choices to lead considerable and consistent improvements over the baselines present in Savva et al. Under a sample budget, performance for RGB-D agents improves 8 SPL on Gibson (14% relative improvement) and 20 SPL on Matterport3D (38% relative improvement). Under a compute budget, performance for RGB-D agents improves by 19 SPL on Gibson (32% relative improvement) and 35 SPL on Matterport3D (220% relative improvement). We hope our findings and recommendations will make serve to make the community's experiments more efficient."
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
url_pdf = "https://arxiv.org/abs/2012.06117"
url_preprint = ""
url_code = "https://github.com/facebookresearch/habitat-lab"
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
image = "pointnav-in-a-day-teaser.jpg"
caption = ""

+++
