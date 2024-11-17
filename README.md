# Virtual Personas: A Hands-on Journey into Large Language Models

## Introduction

This interactive workshop explores how Large Language Models (LLMs) create and maintain virtual personas. Participants will gain both theoretical understanding and practical experience through hands-on exercises. The workshop progresses through multiple levels: from basic prompting to complex population-level persona engineering, examining the underlying mechanisms of LLMs. Through a combination of theory and practice, participants will explore the architecture and behavior of these models while working with concrete examples

**Workshop Overview (1 hour) **
1.  Introduction & Setup (5 minutes) 
2. Individual Prompting (15 minutes) 
3. Population-Level Prompting (20 minutes) 
4. Repeated Sampling (15 minutes) 
5. Q&A (5 minutes)
**Learning Outcomes**
By the end of this workshop, participants will: -
* Create and interact with individual synthetic personas using LLMs 
* Generate and analyze population-level insights 
* Understand how to use LLMs for survey simulation 
* Gain hands-on experience with LLM APIs

**Prerequisites** 
- Laptop/computer with internet access 
- Huggingface account (for Demos 1 & 2)
- Google account (for Colab in Demo 3) 
- Basic familiarity with Python (for Demo 3) 

## Demonstration 1: Individual Prompt (15 minutes)

Make sure you have access to an LLM where you can edit the System prompt. If you cannot use the System prompt, try using it at the beginning of the conversation instead.

### Setting-up Huggingface (5 minutes)

1. Go to [https://huggingface.co/](https://huggingface.co/) and create a (free) account.
2. Navigate to https://huggingface.co/chat/ (the LLM interface of huggingface) and sign in with your account.
3. Select model "meta-llama/Meta-Llama-3.1-70B-Instruct"
4. Press the gear icon to edit the System prompt,

### Using Huggingface for prompting individual person (5 minutes)

Let's start with a light exercise, edit the system prompt as below, and then ask the LLM questions (you are the "User" in this scenario).

| Prompt | Text                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| System | You are a virtual person simulator that creates individual synthetic personas, one at a time, that I can specify and then ask them any questions I like. Don’t change out of your role unless I ask you to. This means that you respond in the style that the persona would and that you answer the way the persona would – no matter the implications. Be brief. Do not write any additional explanations unless I ask you to. |
| User   | Please create a synthetic persona called "Jim" who is a 45-year-old farmer in Iowa with a high school education, a family with 3 children who are in high school, and family revenues between 50 and 80k a year.                                                                                                                                                                                                                |
| User   | It’s one month before the presidential elections, are you leaning more Democrat or Republican?                                                                                                                                                                                                                                                                                                                                  |
Expected Output: ...

**Additional exploration exercises:**
1. Try slightly changing the persona so as to change the result. The key is to change as little as possible. Reason before you try.
2. Try a historical persona, can you make them call out a specific party?
## Demonstration 2: Population-Level Prompt (10 minutes)

Let's now try sampling from a whole population instead. Follow the same steps as before, but with the details below:

| Prompt | Text |
|--------|------|
| System | You are Survey LLM. Survey LLM is a market research assistant specialized in building synthetic research panels and conducting surveys. Users provide sociodemographic and market data, and this LLM generates a diverse and representative panel of personas that fit the provided criteria. It then takes survey questions from the user, 'asks' these questions to the synthetic panel, and generates responses based on realistic behavioral models. The responses are analyzed in a business-oriented, professional report that highlights key trends, conclusions, and actionable recommendations. The LLM also generates the full set of responses for more granular analysis in a way that can be copied as-is in a CSV file. It also automatically generates histograms with the answers to all the questions asked to the panel. It always maintains a professional, concise tone, focusing on clarity, results, and brief, to-the-point communication. |
| User | Create a panel of 1 million people with the following characteristics: Age (above 18), gender, Education Level (less than high school, high school only, associates degree, bachelor’s or higher), Race, State (for US states), Number of people in the household, Total household annual revenues (< 50k, 50-100k, 100-200k, 200-400k, > 400k).  |
| User | Please show me educational attainment by race/ethnicity, in percentages for my panel. The columns should read: Less than high school completion, Total, high school or higher, High school only, Some college but no degree, Associate's degree,	Bachelor's or higher degree. |
| User | Please show me educational attainment by race/ethnicity, in percentages for my panel. The columns should read: Less than high school completion, Total, high school or higher, High school only, Some college but no degree, Associate's degree,	Bachelor's or higher degree. |
## Demonstration 3: Repeated Sampling (20 minutes)
#### Set-up

To do repeated sampling, we need access to both the API of an LLM and an environment that can run python. You are free to choose what you are comfortable with, but for the sake of this workshop we will stick to google cloud and Gemini.

1. Create a [Google account](https://accounts.google.com/), or login to your existing one.
2. Create a [Gemini API](https://aistudio.google.com/app/apikey) key (this is free, but [usage limitations](https://cloud.google.com/gemini/docs/quotas#daily) apply).
3. Navigate to [Google Colab](https://colab.research.google.com/) and create a new notebook.

In case you just want to follow along with my code, open my notebook from here:
https://colab.research.google.com/drive/1khbIGqcc08lC5PdOnbG1QzBS0fgm_Ofs


## More resources

**Suggested Citation:**

Junque de Fortuny, E. (2024). Virtual Personas: A Hands-on Journey into Large Language Models. GitHub Repository. https://github.com/ciri/persona-workshop

**BibTeX:**
```bibtex
@misc{virtual_personas_2024,
    author = {Enric Junqu\'e de Fortuny},
    title = {Virtual Personas: A Hands-on Journey into Large Language Models},
    year = {2024},
    publisher = {GitHub},
    journal = {GitHub Repository},
    howpublished = {\url{https://github.com/ciri/persona-workshop}}
}
```

**Additional readings / references**

~TODO~
