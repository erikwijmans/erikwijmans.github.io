+++
title = "Habitat: A Platform for Embodied AI Research"
date = 2019-04-25T23:13:55-05:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Manolis Savva&ast;", "Abhishek Kadian&ast;", "Oleksandr Maksymets&ast;", "Yili Zhao", "**Erik Wijmans**", "Bhavana Jain", "Julian Straub", "Jia Liu", "Vladlen Koltun", "Jitendra Malik", "Devi Parikh", "Dhruv Batra"]

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
publication = "International Conference on Computer Vision (ICCV)"
oral = "top 187 of 4303 submissions = top-4.3%"
publication_short = ""

# Abstract and optional shortened version.
abstract = "We present Habitat, a new platform for the development of embodied artificial intelligence (AI). Training robots in the real world is slow, dangerous, expensive, and not easily reproducible. We aim to support a complementary approach -- training embodied AI agents (virtual robots) in photorealistic 3D simulation and transferring the learned skills to reality.<br/> The 'software stack' for training embodied agents involves  _datasets_ providing 3D assets,  _simulators_ that render these assets and simulate agents, and _tasks_ that define goals and evaluation metrics, thus enabling controlled and reproducible assessment of scientific progress. We aim to standardize this entire stack by  contributing specific instantiations at each level: unified support for scanned and modelled 3D scene datasets, a new simulation engine (Habitat-Sim), and a modular API (Habitat-API).<br/>  The Habitat architecture and implementation combine modularity and high performance. For example, when rendering a realistic scanned scene from the Matterport3D dataset, habitatsim achieves several thousand frames per second (fps) running single-threaded and can reach over 10,000 fps multi-process on a single GPU.<br/> We also describe the Habitat Challenge, an autonomous navigation challenge that aims to benchmark and accelerate progress in embodied AI."

abstract_short = "We present Habitat, a new platform for the development of embodied artificial intelligence (AI). Training robots in the real world is slow, dangerous, expensive, and not easily reproducible. We aim to support a complementary approach -- training embodied AI agents (virtual robots) in photorealistic 3D simulation and transferring the learned skills to reality.<br/>We also describe the Habitat Challenge, an autonomous navigation challenge that aims to benchmark and accelerate progress in embodied AI."

# Featured image thumbnail (optional)
image_preview = "habitat_logo_text.svg"

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = ""
url_preprint = "https://arxiv.org/abs/1904.01201"
url_code = "https://github.com/facebookresearch/habitat-sim"
url_dataset = "https://github.com/facebookresearch/habitat-api"
url_project = "https://aihabitat.org"
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""

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
image = "habitat_logo_text.svg"
caption = ""

+++

Read more about AI Habitat -- [ai.facebook.com](https://ai.facebook.com/blog/open-sourcing-ai-habitat-an-simulation-platform-for-embodied-ai-research/) and [aihabitat.org](https://aihabitat.org)

Particpate in the Habitat Challenge -- [facebookresearch/habitat-challenge](https://github.com/facebookresearch/habitat-challenge)

Get started using the Habitat-API -- [facebookresearch/habitat-api](https://github.com/facebookresearch/habitat-api) <br/>
and Habitat-Sim --
[facebookresearch/habitat-sim](https://github.com/facebookresearch/habitat-sim)
