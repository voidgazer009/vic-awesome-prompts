# 自由职业者法律风险自查工具（Shield）
> **Legal Risk Minimization Tool for Freelancers**

| 项目 | 内容 |
|---|---|
| 来源 | [f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) · `prompts.csv` |
| 原作者 | mmanisaligil |
| 许可证 | CC0 1.0（公共领域，可自由使用与改编） |
| 适用场景 | 一人公司 / 自由职业者做合同生成与审阅类小工具时的产品需求提示词 |
| Vic 评分 | ★★★★☆ 7/10 |
| 收录日期 | 2026-11-19 |

## 原文 Prompt

```text
Build a legal risk reduction tool for freelancers called "Shield" — a contract generator and reviewer that reduces common legal exposure.

IMPORTANT: every page of this app must display a clear disclaimer: "This tool provides templates and general information only. It is not legal advice. Review all documents with a qualified attorney before use."

Core features:
- Contract generator: user inputs project type (web development / copywriting / design / consulting / photography / other), client type (individual / small business / enterprise), payment terms (fixed / milestone / retainer), approximate project value, and 3 custom deliverables in plain language. [LLM API] generates a complete contract covering scope, IP ownership, payment schedule, revision policy, late payment penalties, confidentiality, and termination — formatted as a clean DOCX
- Contract reviewer: user pastes an incoming contract. AI highlights the 5 most important clauses (ranked by risk), flags anything unusual or asymmetric, and for each flagged clause suggests a specific alternative wording
- Risk radar: user describes their freelance business in 3 sentences — AI identifies their top 5 legal exposure areas with a one-paragraph explanation of each risk and a mitigation step
- Template library: 10 pre-built contract types, all downloadable as DOCX and editable in any word processor
- NDA generator: inputs both party names, confidentiality scope, and duration — generates a mutual NDA in under 30 seconds

Stack: React, [LLM API] for generation and review, docx-js for DOCX export. Professional, trustworthy design — this handles serious matters.
```

## Vic 点评：为什么好

- 每个页面强制显示“非法律意见”免责声明，把合规边界写进需求
- 功能拆得清楚：合同生成、条款审阅（按风险排序并给替换措辞）、风险雷达
- 技术栈与交付格式（DOCX）明确，可直接交给 AI 编程工具

## 改造建议

这是做工具用的提示词，不是对话提示词。使用时把适用法域写明（中国大陆合同与海外合同差异大），并增加“不得编造法条”的规则，合同成品必须由律师复核。
