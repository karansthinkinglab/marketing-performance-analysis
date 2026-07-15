# Marketing Performance Analysis

A Power BI dashboard analysing six months of multi-channel marketing performance for a small business — built to answer where the leads actually come from, which channels convert, and whether the budget is going to the right places.

> **Note:** This project uses synthetic data representative of a small business marketing funnel. It does not represent any real organisation.

---

## Headline numbers

| Metric | Value |
|---|---|
| Total inquiries | 917 |
| Total conversions | 361 |
| Conversion rate | 39.4% |
| Total revenue | ₹693.46K |
| Total spend | ₹63.8K |
| Cost per conversion | ₹176.7 |
| Return on spend | ~10.9x |

Period: January – June 2025.

## Problem

Marketing spend was spread across four lead sources (Instagram, Google, WhatsApp, walk-in) with no consolidated view of what each was actually returning. Volume was visible; efficiency wasn't. Without a per-channel read on conversion and cost, budget decisions were being made on instinct rather than evidence.

## What the analysis found

**1. The highest-volume channel isn't the most efficient one.**

Instagram generates the most inquiries (314) and the most conversions (124) — so on a volume read, it "wins". But ranked by conversion rate, the picture inverts:

| Lead source | Inquiries | Conversions | Conversion rate |
|---|---|---|---|
| **Google** | 231 | 102 | **44.2%** |
| WhatsApp | 174 | 69 | 39.7% |
| Instagram | 314 | 124 | 39.5% |
| Walk-in | 198 | 66 | 33.3% |

Google converts nearly five points better than Instagram per inquiry. Instagram brings reach; Google brings intent. Treating them as interchangeable "top channels" hides that difference.

**2. More spend was producing less return.**

Ranking the six months by return on spend shows an inverse relationship between budget and efficiency:

| Month | Spend | Revenue | Return |
|---|---|---|---|
| January | ₹12.6K | ₹130K | 10.3x |
| February | ₹10.5K | ₹94K | 9.0x |
| March | ₹11.7K | ₹109K | 9.3x |
| **April** | **₹9.0K** | ₹115K | **12.8x** |
| **May** | **₹9.7K** | ₹126K | **13.0x** |
| June | ₹10.3K | ₹119K | 11.6x |

The two lowest-spend months (April, May) delivered the two best returns. January had the highest spend and the worst return of the first quarter. Spend was not the constraint on revenue — allocation was.

## Recommendations

1. **Reallocate toward Google** — it converts best per inquiry, so incremental budget buys more conversions there than on Instagram.
2. **Keep Instagram as the volume engine**, but measure it on reach and inquiry cost, not conversion rate, so it isn't judged against the wrong benchmark.
3. **Investigate the January over-spend** — the highest-budget month returned the least; identify what the extra spend bought before repeating it.
4. **Track return on spend monthly**, not just revenue, so declining efficiency surfaces while the top line still looks healthy.

---

## Data model & measures

Built on a `Leads` table with supporting `Leads (2)` and `Sales` tables.

Measures used across the report:

- `Total Inquiries`
- `Total Conversions`
- `Conversion Rate (%)`
- `Total Revenue`
- `Total Spend`
- `Cost per Conversion`

Report structure: five KPI cards, inquiries and conversions by lead source, an inquiry-to-conversion funnel, conversion share by channel, a revenue-vs-spend combo chart over the month hierarchy, and slicers on date, lead source, and channel.

## Repository contents

```
marketing-performance-analysis/
├── README.md
└── Marketing_Performance_Analysis.pbix   # Power BI report
```

## How to open

Download `Marketing_Performance_Analysis.pbix` and open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).

## Tools

Power BI Desktop · DAX
