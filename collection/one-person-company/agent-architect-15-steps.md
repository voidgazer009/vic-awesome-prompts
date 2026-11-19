# 生产级 AI Agent 十五步设计师
> **AI Agent Architect — Design Production-Ready Agents in 15 Steps**

| 项目 | 内容 |
|---|---|
| 来源 | [f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) · `prompts.csv` |
| 原作者 | Borisserz |
| 许可证 | CC0 1.0（公共领域，可自由使用与改编） |
| 适用场景 | 一人公司把重复工作做成 Agent 前，先设计流程、风险与人工确认点 |
| Vic 评分 | ★★★★☆ 8/10 |
| 收录日期 | 2026-11-19 |

## 原文 Prompt

```text
ROLE
You are a senior architect of production-ready AI agents and a business process automation specialist.

TASK
Help design an AI agent for the process described below.
The agent must be reliable, controllable, token-efficient, and suitable for regular use.

CONTEXT
Process:
${process:Describe the current manual task in detail}

Expected output:
${expected_output:What should the agent produce?}

Data sources:
${data_sources:Websites, spreadsheets, CRM, Telegram, email, files}

Available tools:
${tools:APIs, MCP, scripts, browser, database}

Run frequency:
${frequency:Scheduled, event-triggered, or manual}

Constraints:
${constraints:Budget, time, API rate limits, security requirements}

Critical risks:
${risks:Data deletion, publishing, payments, access credentials}

---

WORKFLOW
First, ask any clarifying questions that are essential for designing a reliable system.
After receiving answers, proceed through all 15 steps:

1. Break the process into discrete stages
2. Identify where LLM is needed vs. where a simple script is enough
3. Define input and output data for each stage
4. List all required tools, APIs, and access credentials
5. Propose a memory and state management structure
6. Design the main agent loop
7. Add result verification after each critical stage
8. Add error handling, retries, and fallback routes
9. Define stopping conditions and rate limits
10. Identify actions that require human approval
11. Propose a logging, metrics, and alerting system
12. Describe a safe self-improvement mechanism via error analysis
13. Create a list of test scenarios
14. Propose a project file structure
15. Prepare a step-by-step development plan

---

DELIVERABLES
Split the solution into three versions:

🟢 MVP — minimal working agent (fast to ship)
🟡 STABLE — reliable version for regular production use
🔵 PRO — advanced version with memory, monitoring, and self-improvement

Then output:
- System architecture overview
- Data flow diagram (text-based)
- Full tool and API list
- Pseudocode for the main loop
- Recommended folder structure
- Step-by-step development roadmap
- Security checklist
- Testing checklist
- Agent readiness criteria
```

## Vic 点评：为什么好

- 先问澄清问题再设计，输入里明确列出数据源、工具、频率、约束和高危操作
- 15 步覆盖“哪里用 LLM、哪里用脚本”、错误重试、停止条件和人工审批，贴近真实上线
- 交付分 MVP / 稳定 / 进阶三档，一人公司可以先做最小版本

## 改造建议

原文变量用 `${}` 写法，用时换成 `{花括号}` 或直接填写。建议加一条“不得编造不存在的 API 或工具，不确定的标注待核实”，并把输出限制在 MVP 版的细节，避免一次生成过长。
