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

[Example Result](https://hf.co/chat/r/kd-N8es?leafId=6fbd123a-aae1-41a7-ba9e-73b70fc76ab8)

**Additional exploration exercises:**
1. Try slightly changing the persona so as to change the result. The key is to change as little as possible. Reason before you try.
2. Try a historical persona, can you make them call out a specific party?

**Take-home exercises:**
1. Try changing the model to Qwen or Allam, notice any differences?
2. Try the same set-up within a domain that you are very familiar with and explore where it works/fails.
