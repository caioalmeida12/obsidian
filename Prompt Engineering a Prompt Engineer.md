> [!NOTE]
> **Large language models (LLMs) are powerful tools for many natural language processing tasks, when provided with the right prompts**. However, **LLMs are also notoriously sensitive to prompt design** (Jiang et al., 2020; Zhao et al., 2021; Reynolds and McDonell, 2021; Lu et al., 2022), and **finding the right prompts often requires extensive manual efforts referred to as “prompt engineering.”** 

<span style="color:rgb(148, 148, 148)">NonAI experts, in particular, may struggle to effectively communicate the task of interest to LLMs, resulting in prompt engineering being performed opportunistically rather than systematically (ZamfirescuPereira et al., 2023). Adding to this challenge, once a high-quality prompt is found and deployed into production, unforeseen edge cases can arise, necessitating more rounds of manual efforts. All these challenges give rise to an emerging research field of automatic prompt engineering. Within this field, a notable line of methods involves leveraging the capabilities of LLMs themselves (Zhou et al., 2023b; Pryzant et al., 2023). This entails meta-prompting LLMs with instructions such as “inspect the current prompt and a batch of examples, provide feedback, then propose a new prompt.” (See Figure 1)</span>

<span style="color:rgb(148, 148, 148)">While these methods achieve impressive performance, a subsequent question arises: What makes a good meta-prompt for automatic prompt engineering? To answer this question, we connect two key observations: </span>

> [!NOTE]
> **(1)** **Prompt engineering, at its core, is a language generation task that requires complex reasoning: it involves closely examining the model’s errors, hypothesizing what is missing or misleading in the current prompt, and communicating the task more clearly to LLMs. (2) Complex reasoning capabilities in LLMs can be elicited by prompting the model to “think step by step” (Wei et al., 2022a; Kojima et al., 2022) and can be further improved by instructing them to reflect on their outputs (Madaan et al., 2023; Chen et al., 2024).**
> 


> [!NOTE] Title
>2.1 Prompt Engineering
>**The goal of prompt engineering is to find the textual prompt p ∗ that achieves the best performance on a given dataset D when using a given LLM Mtask as the task model. More specifically, we assume all datasets can be formatted as textual input-output pairs, i.e., D = {(x, y)}.** 
>We are given a training set Dtrain for optimizing the prompt, Ddev for validation, and Dtest for final evaluation. Following the notations in Zhou et al. (2023b), the prompt 2Both the base-8 addition rules and the model-induced rules hold true for examples like 75+7=104 and 5+6=13. 2 engineering problem can be described as: p ∗ = arg max p X (x,y)∈Ddev f(Mtask(x; p), y) (1) where Mtask(x; p) is the output generated by the task model when conditioning on the prompt p, and f is a per-example evaluation function. For example, if the evaluation metric is exact match, f(Mtask(x; p), y) = 1[Mtask(x; p) = y].



#tcc/fonte 