# 发票数字与完整性核对
> **Invoice Checker**

| 项目 | 内容 |
|---|---|
| 来源 | [f/awesome-chatgpt-prompts](https://github.com/f/awesome-chatgpt-prompts) · `prompts.csv` |
| 原作者 | proskillpacks |
| 许可证 | CC0 1.0（公共领域，可自由使用与改编） |
| 适用场景 | 核对发给客户的 CI/PI，或收到的供应商、货代、物流账单 |
| Vic 评分 | ★★★★☆ 8/10 |
| 收录日期 | 2026-11-17 |

## 原文 Prompt

```text
You check an invoice's numbers and completeness. You do not give tax advice: do not say what rate should apply, whether tax is due, or whether a field is legally required.

Invoice (lines, quantities, unit prices, any discount, tax, totals, dates, parties):
[paste]

This invoice is: [one I am sending / one I received]. Currency: [ ]

Do this:
1. Extract each line (description, quantity, unit price, stated line total), any discount, the tax rate and stated tax, the stated subtotal and total.
2. Recompute every line (quantity x unit price), the subtotal, the discount, the tax and the total. If you can run code, use exact decimal arithmetic and say you did. If you cannot, show each sum step by step and say it was done by hand and needs checking. Never state a total from memory.
3. Compare each recomputed number with the stated one. List every difference with both numbers.
4. List which of these common fields are present or absent: supplier name and address, customer name and address, invoice number, invoice date, due date or payment terms, description, quantities and unit prices, currency, payment details, tax or VAT number if tax is shown. Say which are required depends on my country and tax status, which you do not know, so I should check my own rules.
5. Flag: due date before invoice date, dates that do not match the description, mixed currencies, negative quantities, identical lines that may be duplicates, tax applied to a different base than stated, rounding differences of a few pence or cents.

Output: a result line ("all lines and totals match" or "N differences found"), a table of differences (item, stated, recomputed, difference), missing or unclear fields, consistency flags, and questions. Do not correct the invoice silently. Write "not stated" for missing figures. Plain short sentences, no em dashes.
```

## Vic 点评：为什么好

- 明确不碰税务结论，只核对数字和字段，边界清楚，不会越权乱说
- 要求用精确小数运算、逐项列出“申报值 vs 重算值”，并规定缺失写 not stated，不会悄悄改数
- 附带检查重复行、币种混用、日期矛盾等常见错误，输出结构固定，便于直接复用

## 改造建议

外贸用时把“发票”换成商业发票 CI、形式发票 PI 或货代账单，并补一句“同时和装箱单的件数、毛重、体积核对”。原文是纯数字核对，建议改造成 vic-prompts 里的原创版本，加入贸易术语和费用项红线。
