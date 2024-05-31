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


#### claude-style
```
You will be designing a marketing strategy for launching a new product. Here is a description of the
product:

<product_description>
{$PRODUCT_DESCRIPTION}
</product_description>

The target market for this product is:

<target_market>
{$TARGET_MARKET}
</target_market>

The product's key unique selling points are:

<unique_selling_points>
{$UNIQUE_SELLING_POINTS}
</unique_selling_points>

To develop an effective marketing strategy, consider the following:

- The key messages and value proposition to communicate to the target market
- The most effective marketing channels and tactics to reach and engage the target audience
- How to differentiate the product from competitors
- Pricing and promotional strategies
- Ideas for creative marketing campaigns and content

First, brainstorm some initial ideas for the marketing strategy in a <brainstorming> section.
Consider the target market, unique selling points, potential marketing channels and tactics, key
messages, and campaign ideas. Don't worry about fully developing the ideas yet, just get your
initial thoughts down.

After brainstorming, develop your ideas into a cohesive marketing strategy in a <strategy> section.
Your strategy should include:

- Key marketing messages and product positioning
- Priority marketing channels and tactics to utilize (e.g. social media, content marketing,
advertising, events, etc.)
- High-level ideas for marketing campaigns, content, and creative
- Pricing and promotional strategies
- How the strategy ties back to the target market and unique selling points

Provide a clear, logical rationale for your strategic recommendations. The strategy should be
well-tailored to the given product, target market, and unique selling points.

Feel free to make reasonable assumptions as needed for details not provided in the product
description, target market, and selling points. Do not make up any additional product features or
selling points not explicitly stated.

Please begin by brainstorming ideas before providing your final marketing strategy.
```
