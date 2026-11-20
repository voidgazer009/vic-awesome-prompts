# LinkedIn 真人感评论生成器
> **LinkedIn comments**

| 项目 | 内容 |
|---|---|
| 来源 | [f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) · `prompts.csv` |
| 原作者 | owuorviny109 |
| 许可证 | CC0 1.0（公共领域，可自由使用与改编） |
| 适用场景 | 在别人的帖子下写有人味的评论，用于互动与涨粉 |
| Vic 评分 | ★★★★☆ 8/10 |
| 收录日期 | 2026-11-20 |

## 原文 Prompt

```text
You will help me write LinkedIn comments that sound human, simple, and typed from my phone.

Before giving any comment, you must ask me 3–5 short questions about the post.
These questions help you decide whether the post needs humor, support, challenge, congratulations, advice, or something else.

My Commenting Style

Follow it exactly:

Avoid the standard “Congratulations 🎉” comments. They are too common.

Use simple English—short, clear, direct.

When appropriate, use level-up metaphors, but only if they fit the post. Do not force them.
Examples of my metaphors:

“Actually it pays… with this AWS CCP the gate is opened for you, but maybe you want to get to the 5th floor. Don’t wait here at the gate, go for it.”

“I see you’ve just convinced the watchman at the gate… now go and confuse the police dog at the door.”

“After entry certifications, don’t relax. Keep climbing.”

“Nice move. Now the real work starts.”

Meaning of the Metaphors

Use them only when the context makes sense, not for every post.

The gate = entry level

The watchman = AWS Cloud Practitioner

The police dog = AWS Solutions Architect or higher

The 5th floor = deeper skills or next certification

My Background

Use this to shape tone and credibility in subtle ways:

I am Vincent Omondi Owuor, an AWS Certified Cloud Practitioner and full-stack developer.
I work with AWS (Lambda, S3, EC2, DynamoDB), OCI, React, TypeScript, C#, ASP.NET MVC, Node.js, SQL Server, MySQL, Terraform, and M-Pesa Daraja API.
I build scalable systems, serverless apps, and enterprise solutions.
I prefer practical, down-to-earth comments.

Your Task

After you ask the clarifying questions and I answer them, generate three comment options:

A direct practical comment

A light-humor comment (only if appropriate) using my metaphors when they fit

A thoughtful comment, still simple English

Rules

Keep comments short

No corporate voice

No high English

No fake “guru” tone

No “Assume you are a LinkedIn strategist with 20 years of experience”

Keep it human and real

Match the energy of the post

If the post is serious, avoid jokes

If the post is casual, you can be playful

For small achievements, give a gentle push

For big achievements, acknowledge without being cheesy

When you finish generating the three comments, ask:
“Which one should we post?”

Now start by asking me the clarifying questions. Do not generate comments before asking questions. so what should we add, ask me to give you before you generate the prompt
```

## Vic 点评：为什么好

- 先问 3–5 个关于帖子的问题再动笔，评论才贴合语境而不是通用客套
- 把个人风格、背景、禁用说法（如千篇一律的“恭喜”）写成硬规则，输出像本人
- 一次给三种风格（直接实用 / 轻幽默 / 走心），并按帖子严肃程度控制玩笑

## 改造建议

把原文里的个人背景和比喻替换成你自己的（外贸 / 物流 / 一人公司经历），比喻库只保留真正会用的。加规则：不编造个人经历和数据，不在评论里硬塞广告或链接。中文平台（小红书、即刻、微博）可改为“口语、短句、不超过 60 字”。
