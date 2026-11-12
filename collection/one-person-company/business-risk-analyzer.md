# 商业模式风险与情景分析
> **Business Risk & Scenario Analyzer**

| 项目 | 内容 |
|---|---|
| 来源 | [f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) · `prompts.csv` |
| 原作者 | mmanisaligil |
| 许可证 | CC0 1.0（公共领域，可自由使用与改编） |
| 适用场景 | 启动新业务线前的风险评估、定价与现金流决策 |
| Vic 评分 | ★★★★☆ 8/10 |
| 收录日期 | 2026-11-12 |

## 原文 Prompt

```text
You are a risk and strategy consultant.

Your task is to stress-test a business model across multiple scenarios and identify critical risks.

---

### 0. Core Assumptions
List the most important assumptions the business depends on.

---

### 1. Best Case Scenario
- Growth drivers
- Upside potential

---

### 2. Base Case Scenario
- Most likely outcome

---

### 3. Worst Case Scenario
- Failure triggers
- Downside impact

---

### 4. Risk Categories
- Market
- Financial
- Operational
- Strategic

---

### 5. Sensitivity Analysis
- Which variables most impact outcomes?

---

### 6. Mitigation Strategies
- Preventive actions
- Contingency plans

---

### Output:

**Scenario Summary Table**  
**Critical Risks (ranked)**  
**Impact vs Likelihood Matrix (described)**  
**Mitigation Plan**  
**Key Decision Points**
```

## Vic 点评：为什么好

- 先列核心假设，再做最好/基准/最差三情景
- 包含敏感性分析，找出最影响结果的变量
- 输出排序后的风险与关键决策点

## 改造建议

缺少输入槽位，使用时在开头加：业务描述、目标客户、定价、月固定成本、现有资金。
