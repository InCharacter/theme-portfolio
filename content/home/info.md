---
# An instance of the Blank widget.
# Documentation: https://wowchemy.com/docs/getting-started/page-builder/
widget: blank

# Activate this widget? true/false
active: true

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 40

title: About InCharacter
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

Do Role-Playing Agents (RPAs) Capture Personalities of the Intended Characters?

## Introduction: Personality Fidelity for RPA Evaluation

Recent advancements in LLMs have catalyzed the emergence of RPAs. However, the evaluation of _character fidelity_
in RPAs remains underexplored. Specifically, do RPAs exhibit stable personalities consistent with the intended characters? How can we measure the personalities of RPAs? Our research, presented in our new paper titled "[InCharacter: Evaluating Personality Fidelity in Role-Playing Agents through Psychological Interviews](http://arxiv.org/abs/2310.17976)", explores just that!


## The Procedure of Personality Tests on RPAs

To evaluate the personality fidelity of RPAs, we apply various scales to measure their personalities and compare the results with the personality labels of the characters. 

<center class="half">
  <img src="/uploads/front.png" width="50%"/>
</center>

Overcoming drawbacks of previous self-report assessments on RPAs, we propose _InCharacter_, namely **In**terviewing **Character** agents for personality tests. The framework of InCharacter for personality tests on RPAs is illustrated below. **Left**: Previous methods use self-report scales, which prompt LLMs to select an option directly. **Right**: InCharacter adopts an interview-based approach comprising two phases: the interview and assessment phases. The interview phase elicits the behavioral, cognitive and emotional patterns of RPAs that reflect their underlying mindsets. The assessment phase measures personalities based on interview results, with two alternative methodologies: option conversion (OC) and expert rating (ER).

<center class="half">
  <img src="/uploads/main.png" width="100%"/>
</center>



## Can State-of-the-art LLMs be Applied to Evaluate Personalities of RPAs (or even Humans)? 

We first validate the capability of interviewer LLMs on the OC and ER tasks given the interview results of RPAs. We compare their predictions with human judgments. The results presented below demonstrate that state-of-the-art LLMs achieve acceptable performance in simulating human interviewers to assess RPA personalities. 

<center class="half">
  <img src="/uploads/table1.png" width="50%"/>
</center>

Then, we apply the personality test methods on 32 popular RPAs from ChatHaruhi and RoleLLM, on two popular psychological scales including the Big Five Inventory (BFI) and the 16Personalities (16P). We match the predicted personalities with human-annotated groundtruth labels. The results are demonstrated below. Using InCharacter~with ER and GPT-4, the measured RPA personalities are highly aligned with groundtruth labels of corresponding characters.This suggests that state-of-the-art RPAs reproduce many of the characters' personality traits well, and our method can accurately measure their personalities compared with the baselines. 

<center class="half">
  <img src="/uploads/table2.png" width="100%"/>
</center>

With InCharacter, we also demonstrate the robustness, consistency and distinctiveness of RPA personalities.

Furthermore, we extend personality tests on RPAs to 14 psychological scales. Overall, we observe that state-of-the-art RPAs exhibit personalities align with the target characters in comprehensive aspects with an average accuracy of 78.9%, covering personality traits (BFI, 16P), dark personalities (DTDD), interpersonal relationships (BSRI, ECR-R), basic interests (CABIN), motivation (GSE, LMS) and emotional intelligence (EIS, WLEIS), e.t.c.

<center class="half">
  <img src="/uploads/radar.png" width="50%"/>
</center>

## Personality Fidelity of RPAs with Different Character Data and Foundation Models

With InCharacter, we compare the personality fidelity of various types of RPAs, covering different character data and foundation models. For character data, we find that RPAs with both descriptions (D) and memories (M) achieve the best fidelity. However, with only descriptions or memories, they can also reproduce character personalities to some extent. For foundation models, we observe that RPAs with GPT-3.5 and GPT-4 achieve the best personality fidelity, and GPT-4 does not significantly surpass GPT-3.5. Besides, increamental fine-tuning on role-playing datasets effectively improves personaltiy fidelity of the open-source LLMs. Interesting, character.ai RPAs barely reproduce the personalities, and we notice that their answers tend to be compliant and pleasing to users, instead of reproducing the characters.

<center class="half">
  <img src="/uploads/table3.png" width="70%"/>
</center>

## Case Studies

To illustrate the vividness of state-of-the-art RPAs' personalities, we demonstrate the example responses on the Openness dimension of the BFI and the Perception/Judging dimension of the 16P, from RPAs with low and high scores. 

<center class="half">
  <img src="/uploads/case.png" width="100%"/>
</center>

Besides, we visualize the measured personalities of the state-of-the-art RPAs and the annotated personalities of corresponding characters via radar charts.

<center class="half">
  <img src="/uploads/bfi_radar.png" width="100%"/>
</center>