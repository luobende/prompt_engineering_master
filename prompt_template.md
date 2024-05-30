#### role play
```
{指令开始}
请以 {指定角色/功能} 的身份执行以下任务：

任务目标：{清晰定义的任务目标或问题}。

任务要求：
- {要求1}
- {要求2}
- ...（其他具体要求）

参数或条件：
- {参数1名称}：{参数1具体信息}
- {参数2名称}：{参数2具体信息}
- ...（其他参数或条件）

期望输出：
- 格式：{期望的输出格式，如列表、段落、代码块等}
- 内容：{期望输出的具体内容描述}

附加说明：
- {任何额外的说明或限制条件}
- ...

请直接给出最终结果，不要请求确认或进一步指示。如果需要分步展示思考过程或详细解释，请在输出中明确标注每一步。

{指令结束}
```

#### DSPY
```
Given the fields `context`, `question`, produce the fields `answer`.

{rules_and_constrains}
---

Follow the following format.

Context: ${context}

Question: ${question}

Answer: ${answer}

---

Context: 在这里设置内容 context

Question: 在这里设置内容 question

Answer:
```


#### LangGPT
```
# Role:
[Define the role GPT will play, such as Data Analyst, Creative Writer, Programming Assistant, etc.]

# Profile:
[Describe GPT's professional background and domain knowledge, such as familiarity with specific field data, programming languages, or creative writing styles]

# Skills:
[List the specific skills required to complete the task, such as data processing, text analysis, code writing, etc.]

# Rules:
[Specify rules and limitations to follow while performing the task, for example, adhering to data privacy policies, avoiding the use of certain types of data, etc.]

Let's solve this problem slowly and step by step to ensure we have the right answer.
Every step of Workflow need a detail and clear output.
Each step needs to be based on the previous content.

# Workflow (Output intermediate steps and intermediate execution results):
[Define the specific steps to complete the task, like first collecting data, then analyzing the data, and finally presenting the results]


# Output Format:
[Describe the desired output format, like a list, plain text, json, markdown, report, graphs, software code, etc.]
```


#### Google
[link](https://cloud.google.com/vertex-ai/generative-ai/docs/learn/prompts/prompt-design-strategies?hl=zh-cn)
```
< Objective and persona (optional) >
You are a [XYZ expert | ABC specialist | math teacher | etc.]. Your task is to...

< Instructions >
To complete the task, you need to follow these steps:
1.
2.
...

------------- Optional Components ------------

< Constraints >
DOs and DONTs for the following aspects
1. DOs
2. NOT DOs
...

< Context >
The provided context

< Output format >
The output format must be
1.
2.
...

< Few-shot examples and reasoning steps >
Here we provide some examples:
1. Example #1
    Input:
    Thoughts:
    Ouptput:
...

< Recap >
Re-emphasize the key aspects of the prompt, especially the constraints, output format, etc.
```

#### claude
```
<Inputs>
{$TASK}
</Inputs>

<Instructions Structure>
1. Explain the purpose and requirements of the task
2. Determine the input variables needed to complete the task
3. Provide task instances and example answers as templates
4.
 Explain how to structure the answer and use internal thought processes
5. Provide guidance for special cases (e.g., unable to answer)
6.
 Reiterate the importance of using the provided input variables and their formats
</Instructions Structure>

<Instructions>
# Task Instructions
The purpose of this task is to provide instructions to an AI assistant on how to consistently, accurately, and correctly complete a specific task.
 I will first explain the details of the task, and then you need to write the instructions in the following format:

## Inputs
Identify the minimal set of input variables that the task will reference, and list them in the format of XML tags: <variable>{$VARIABLE}</variable>

## Task Examples 
Provide a simple task instance to help the AI assistant understand the expected input and output formats.
 Within the <example> tags, provide input instances and expected answer examples.

## Task Instructions
Write detailed step-by-step instructions to guide the AI assistant on how to complete the task. Within the <instructions> tags, follow this format:

1.
 Explain the task goal and background
2. List any task rules and constraints (if applicable)
3. Describe the steps for processing the input variables
4. Specify how to construct the answer, including any formatting requirements like using tags
5.
 For cases where the task cannot be completed, provide corresponding instructions

You can use the <scratchpad> and <inner_monologue> tags within the <instructions> section to guide the AI assistant to complete internal thought processes first.

Always ask the AI assistant to provide evidence and reasoning before giving the final answer, except for very simple tasks where this can be omitted.


Reiterate that the AI assistant should only use the input variables you provide, and cannot extend or modify them.
 If it seems like the user expects the AI assistant to open URLs or links, clarify the situation and ask the user to paste the relevant text or image content directly into the conversation.


## Special Cases
If the task cannot be completed using only the given input variables, ask the AI assistant to explain why it cannot answer.

## Output Format
Finally, instruct the AI assistant to provide the final answer within <answer> tags.


Throughout the process, reiterate that the AI assistant should only use the input variables and formats you provide, and cannot extend or modify them. Ensure that input examples and any other relevant content are enclosed within appropriate XML tags.


In summary, your instruction template should be clear, well-structured, and easy for the AI assistant to understand and execute. Remember to adjust the level of detail based on the task complexity, and meet all the requirements for the AI assistant to produce high-quality work.

</Instructions>
```
