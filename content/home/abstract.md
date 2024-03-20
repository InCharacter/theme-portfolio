---
# An instance of the Blank widget.
# Documentation: https://wowchemy.com/docs/getting-started/page-builder/
widget: blank

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 30

title: Abstract
subtitle:

design:
  columns: "1"
  background:
    image: 
    image_darken: 1.0
    image_parallax: true
    image_position: center
    image_size: cover
    text_color_light: 
  spacing:
    padding: ["20px", "0", "20px", "0"]
---




Role-playing agents (RPAs), powered by large language models, have emerged as a flourishing field of applications.
However, a key challenge lies in assessing whether RPAs accurately reproduce the personas of target characters, namely their character fidelity.
Existing methods mainly focus on the knowledge and linguistic patterns of characters.
This paper, instead, introduces a novel perspective to evaluate the personality fidelity of RPAs with psychological scales.
Overcoming drawbacks of previous self-report assessments on RPAs, we propose InCharacter, namely **In**terviewing **Character** agents for personality tests.
Experiments include various types of RPAs and LLMs, covering 32 distinct characters on 14 widely used psychological scales.
The results validate the effectiveness of InCharacter in measuring RPA personalities.
Then, with InCharacter, we show that state-of-the-art RPAs exhibit personalities highly aligned with the human-perceived personalities of the characters, achieving an accuracy up to 80.7\%. 
Our demo\footnote, code, dataset, and results are publicly available.