# Methods

The protocol below is the one used in later bake-offs, teardowns, and ledger updates. It should not be quietly changed from post to post to make a product look better or worse. If the method itself has to change, the change will be dated here.

Times and test dates use Asia/Shanghai unless a file says otherwise.

## Coding-agent bake-offs

The reference repository is a small C/C++ or Go service maintained for this work. Every tool in a given bake-off gets the same repository snapshot and the same written instructions. The prompt is not tuned for one vendor.

There are four fixed tasks:

1. Fix a failing test and make it pass.
2. Perform a cross-file refactor.
3. Fix a bug planted in advance.
4. Add a small feature from a short requirement written in Chinese.

Only the fields in `coding-agent-scorecard.csv` are scored. The polish of a tool's explanations is not scored.

| Field | What is recorded |
| --- | --- |
| Independent completion | Yes, no, or partial |
| Human interventions | Count of times a human had to step in |
| Tests | Pass or fail on the final state |
| Diff cleanliness | Whether the change is scoped, or noisy with unrelated files, formatting churn, or leftover comments |
| Time | Wall-clock minutes |
| Data leaving the machine | Yes, no, or unclear, plus what was observed |

Each bake-off also records the test date, the exact product and plan, and any signup or billing friction that would matter to an overseas reader.

The first planned bake-off is Trae, Qoder CN, and Cursor on the same repository. Cursor is a global baseline, not the subject of a Cursor review. Qoder CN is Alibaba Cloud's domestic coding product, formerly 通义灵码, renamed in May 2026, and is easy to confuse with the international Qoder product. If a domestic tool cannot be opened, CodeBuddy or Comate may be substituted. At least one domestic product and one global baseline will be kept, and the task set will not change.

## API and application teardowns

Each teardown uses the fields in `teardown-record.csv`.

| Field | What is recorded |
| --- | --- |
| Test date | Calendar date, Asia/Shanghai |
| Product and surface | Exact model, API, or application, including the version or plan shown at test time |
| Signup friction | What an overseas reader hits when creating an account or enabling billing |
| Official list price | From the official page on the test date, with a link |
| Measured unit cost | On a fixed, published workload |
| Measured latency | On the same workload |
| Quality | On a fixed, published evaluation set |
| Limits | Rate limits, region, context length, or gated features |
| Data handling | What official docs and the product UI say, and what was observed |
| Falsifiers | What would change the write-up |

Conclusions are not pre-written. The official price is whatever the vendor's page says on the day of the test.

The first planned teardown is the DeepSeek API: published price versus a real workload, including official peak and off-peak windows as they stand on the test date. A U.S. API will be added as a comparison only if billing can actually be opened.

## Ledger

See [`../ledger/`](../ledger/). One table is updated over time. Corrections are dated amendments.

## Using AI tools

AI tools may be used to edit English prose and to draft short Chinese briefs in the essays. They are not used to invent evaluation scores, logs, or citations. If a number appears in this repository, it comes from a run that was performed, or from an official page on a dated visit.
