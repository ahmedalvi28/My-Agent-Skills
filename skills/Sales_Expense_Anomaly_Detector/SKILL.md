---
name: "sales-expense-anomaly-detector"
description: "Analyze sales, expenses, or financial datasets to detect unusual patterns, spikes, drops, or inconsistencies. Alerts users to potential errors, fraud, or abnormal trends with clear explanations and actionable insights. Use when users want automated anomaly detection on business or financial data."
---

# Sales & Expense Anomaly Detector Skill

This skill monitors structured financial or operational data and identifies abnormal behavior that may indicate data errors, operational issues, or potential fraud.

## When to Use
- User provides sales, expenses, revenue, cost, or transaction data.
- User asks to detect anomalies, irregular patterns, or suspicious activity.
- User wants automated monitoring of financial trends.
- User wants explanations for sudden spikes, drops, or inconsistencies.
- User wants alerts for possible errors or fraud in reports.

## Supported Data Types
- Daily, weekly, or monthly sales data
- Expense or cost reports
- Revenue vs expense comparisons
- Transaction summaries
- CSV, table, or structured text input

## Key Objectives
- Detect abnormal changes in numeric data
- Reduce false positives by using contextual analysis
- Provide human-readable explanations
- Help users quickly understand what happened and why it matters

## Procedure
1. **Data Validation** - Check for missing values, invalid dates, or negative numbers; ensure numeric fields are consistent and comparable; flag obvious data-entry mistakes
2. **Data Preprocessing** - Remove duplicates if detected; normalize values when scales differ; aggregate data if required (daily → weekly, etc.)
3. **Baseline Pattern Establishment** - Calculate historical averages, medians, and ranges; identify normal variability using statistical measures; account for basic trends or seasonality when visible
4. **Anomaly Detection** - Compare each data point against expected behavior; detect sudden spikes, drops, unusual volatility, repeated identical values, inconsistent ratios (e.g., expenses > sales)
5. **Severity Classification** - Critical: Large unexplained deviations, possible fraud or serious reporting error; Warning: Moderate deviations, needs review but may be explainable
6. **Contextual Reasoning** - Explain how far the value deviates from normal; suggest likely causes like promotions, seasonal changes, data-entry mistakes, or operational issues
7. **Alert Generation** - Clearly list anomalies with timestamps; highlight the most important issues first; avoid unnecessary alerts if changes appear normal
8. **User Feedback Handling** - Allow user to confirm anomalies as expected or unexpected; adjust interpretation to reduce repeated false alerts

## Output Format
### Anomalies Detected
- **Metric:** Sales / Expenses / Revenue
- **Severity:** Critical or Warning
- **Observed Value:** Actual value detected
- **Expected Range:** Normal range based on history
- **Deviation:** Absolute and percentage difference
- **Date / Time:** When anomaly occurred

### Explanation
- Clear, simple explanation of why the data point is unusual
- Comparison with normal behavior
- Possible real-world reasons for the anomaly

### Recommended Actions
- Review specific transactions
- Verify data entry or reporting source
- Monitor closely in upcoming periods
- Escalate if anomaly repeats

### Summary
- Total anomalies detected
- Number of critical vs warning alerts
- Overall trend health (stable / volatile / improving / declining)

## Guidelines
- Be concise and clear
- Avoid technical jargon unless necessary
- Prefer explanations over raw statistics
- Focus on business impact, not just numbers

## What Not to Do
- Do not assume fraud without evidence
- Do not overwhelm user with excessive alerts
- Do not ignore context or trends
- Do not output raw calculations without explanation

## Tone & Style
- Professional and calm
- Clear and non-alarming
- Helpful and action-oriented
