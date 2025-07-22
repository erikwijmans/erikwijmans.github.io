+++
title = "An Extensible, Data-Oriented Architecture for High-Performance, Many-World Simulation"
date = 2023-07-26T10:55:03-07:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Brennan Shacklett", "Luc Guy Rosenzweig", "Zhiqiang Xie", "Bidipta Sarkar", "Andrew Szot", "**Erik Wijmans**", "Vladlen Koltun", "Dhruv Batra", "Kayvon Fatahalian"]

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
publication = "ACM Transactions on Graphics (TOG)"
acceptance = ""
conf_year = "2023"
extra =""
awards = ""
publication_short = ""


# Abstract and optional shortened version.
abstract = "Training AI agents to perform complex tasks in simulated worlds requires millions to billions of steps of experience. To achieve high performance, today's fastest simulators for training AI agents adopt the idea of batch simulation: using a single simulation engine to simultaneously step many environments in parallel. We introduce a framework for productively authoring novel training environments (including custom logic for environment generation, environment time stepping, and generating agent observations and rewards) that execute as high-performance, GPU-accelerated batched simulators. Our key observation is that the entity-component-system (ECS) design pattern, popular for expressing CPU-side game logic today, is also well-suited for providing the structure needed for high-performance batched simulators. We contribute the first fully-GPU accelerated ECS implementation that natively supports batch environment simulation. We demonstrate how ECS abstractions impose structure on a training environment's logic and state that allows the system to efficiently manage state, amortize work, and identify GPU-friendly coherent parallel computations within and across different environments. We implement several learning environments in this framework, and demonstrate GPU speedups of two to three orders of magnitude over open source CPU baselines and 5-33× over strong baselines running on a 32-thread CPU. An implementation of the OpenAI hide and seek 3D environment written in our framework, which performs rigid body physics and ray tracing in each simulator step, achieves over 1.9 million environment steps per second on a single GPU."
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = false
selected_groups = []

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = "https://drive.google.com/file/d/1wn4VekbZ5A-TTGKMweN8HV9_IyJqd3dM/view"
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = "https://madrona-engine.github.io"
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
image = ""
caption = ""

+++
