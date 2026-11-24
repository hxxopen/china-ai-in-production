# Ledger

A dated cost-and-quality ledger of Chinese model APIs, retested with the same method.

`ledger.csv` is the current table. It is version 0.1 in structure only; it has no measured rows yet. The starting basket is DeepSeek, Qwen, Doubao, Kimi, and GLM, as many as can actually be opened. If a product cannot be opened, it will be omitted, with a reason, rather than guessed.

## Columns

| Column | Meaning |
| --- | --- |
| date | Test date, Asia/Shanghai |
| product | Exact product or model |
| official_list_price | Official price on that date, with currency and unit |
| official_price_url | Link to the official page used that day |
| measured_unit_cost | What was actually spent on the fixed workload, reduced to a unit cost |
| latency | Measured latency on that workload |
| quality | Result on the fixed evaluation |
| notes | Limits, caveats, or links to raw records |
| amendment_of | If this row corrects an earlier one, the date and product of the row it amends; otherwise empty |

If a number is corrected, the old row stays, and a new row is added with `amendment_of` filled in.
