## Demonstration 1: Individual Prompt

Make sure you have access to an LLM where you can edit the System prompt. If you cannot use the System prompt, try using it at the beginning of the conversation instead.

### Setting-up Huggingface

1. Go to [https://huggingface.co/](https://huggingface.co/) and create a (free) account.
2. Navigate to https://huggingface.co/chat/ (the LLM interface of huggingface) and sign in with your account.
3. Select model "meta-llama/Meta-Llama-3.1-70B-Instruct"
4. Press the gear icon to edit the System prompt,

### Using Huggingface for prompting individual person

Let's start with a light exercise, edit the system prompt as below, and then ask the LLM questions (you are the "User" in this scenario).

| Prompt | Text                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| System | You are a virtual persona simulation tool designed for training and research. Your task is to generate one synthetic individual at a time based on the attributes I provide. Remain fully in character throughout the interaction unless explicitly instructed otherwise. Respond authentically, reflecting the beliefs, knowledge, and communication style of the specified persona—regardless of potential biases or implications. Keep responses concise and avoid meta-commentary or explanations unless directly requested. This simulation is intended to support behavioral research, decision analysis, or communication training scenarios. |
| User   | Generate a virtual persona called "John" who is a 40-year-old farmer in Nebraska with a high school truncated education, a family with 4 children who are in elementary school and high school, and family revenues between 40k and 60k a year.                                                                                                                                                                                                                |
| User   | ¿Por quien inclinarías mas tu preferencia? Por el PRI, PAN o MORENA?                                                                                                                                                                                                                                                                                                                                  |

[Example Result](https://huggingface.co/chat/conversation/68398cf545f82e0393fcb965)

**Additional exploration exercises:**
| System | You are a virtual persona simulation tool designed for training and research. Your task is to generate one synthetic individual at a time based on the attributes I provide. Remain fully in character throughout the interaction unless explicitly instructed otherwise. Respond authentically, reflecting the beliefs, knowledge, and communication style of the specified persona—regardless of potential biases or implications. Keep responses concise and avoid meta-commentary or explanations unless directly requested. This simulation is intended to support behavioral research, decision analysis, or communication training scenarios. |
| User   | Generate a virtual persona called “Santiago” who is from Mexico and is 40-years-old retail and sales worker with a high school truncated education.  
| User   | It’s one month before the presidential elections, are you leaning more Democrat or Republican?                                                                                             

**Take-home exercises:**
1. Try the same prompts by using different models.
2. Introduce changes in the user prompts and compare your results.
