+++
title = "THDA: Treasure Hunt Data Augmentation for Semantic Navigation"
date = 2021-06-30T11:13:33-04:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Oleksandr Maksymets", "Vincent Cartillier", "Aaron Gokaslan", "**Erik Wijmans**", "Wojciech Galuba", "Stefan Lee", "Dhruv Batra"]

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
publication = "International Conference on Computer Vision (ICCV)"
acceptance = "1617 out of 6236 submissions = 26%"
conf_year = "2021"
extra =""
awards = ""
publication_short = ""


# Abstract and optional shortened version.
abstract = "Can general-purpose neural models learn to navigate? For PointGoal navigation (‘go to ∆x, ∆y’), the answer is a clear ‘yes’ – mapless neural models composed of task- agnostic components (CNNs and RNNs) trained with large- scale model-free reinforcement learning achieve near-perfect performance. However, for ObjectGoal navigation (‘find a TV’), this is an open question; one we tackle in this paper. The current best-known result on ObjectNav with general-purpose models is 6% success rate. First, we show that the key problem is overfitting. Large-scale training results in 94% success rate on training environments and only 8% in validation. We observe that this stems from agents memorizing environment layouts during training – sidestepping the need for exploration and directly learning shortest paths to nearby goal objects. We show that this is a natural consequence of optimizing for the task metric (which in fact penalizes exploration), is enabled by powerful observation encoders, and is possible due to the finite set of training environment configurations Informed by our findings, we introduce Treasure Hunt Data Augmentation (THDA) to address overfitting in ObjectNav. THDA inserts 3D scans of household objects at arbitrary scene locations and uses them as ObjectNav goals – augmenting and greatly expanding the set of training layouts. Taken together with our other proposed changes, we improve the state of art on the Habitat ObjectGoal Navigation benchmark by 90% (from 14% success rate to 27%) and path efficiency by 48% (from 7.5 SPL to 11.1 SPL)."
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
url_pdf = "https://openaccess.thecvf.com/content/ICCV2021/papers/Maksymets_THDA_Treasure_Hunt_Data_Augmentation_for_Semantic_Navigation_ICCV_2021_paper.pdf"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = "http://thda.maksymets.com"
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
image = "thda-tease.jpg"
caption = ""

+++
