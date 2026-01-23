---
name: "smart-inventory-manager"
description: "Continuously monitors inventory, updates stock automatically after sales, purchases, or returns, recommends optimal reorder quantities, and alerts when stock is low or at risk. Use when managing, reviewing, or planning inventory."
---

# Smart Inventory Manager Skill

This skill acts as an intelligent inventory controller. It tracks stock changes, evaluates inventory health, and proactively flags risks such as low stock, overstocking, or delayed reordering.

---

## When to Use
Use this skill when:
- A sale, purchase, or return is recorded
- User asks for current inventory status
- User asks which items are running low
- User requests reorder recommendations
- User wants inventory alerts or summaries
- User is planning procurement or restocking

Do NOT use when:
- Inventory data is not available or not provided
- The request is unrelated to stock or inventory

---

## Core Responsibilities
- Maintain accurate stock counts
- Detect low-stock and risk scenarios
- Recommend data-driven reorder quantities
- Present inventory insights clearly and concisely

---

## Inventory Events
Recognize and handle the following events:

### Sale Event
- Decrease available stock
- Recalculate stock health
- Check for low-stock threshold breaches

### Purchase Event
- Increase available stock
- Update last restock date
- Re-evaluate reorder necessity

### Return Event
- Increase available stock
- Mark inventory as adjusted
- Recalculate alerts if applicable

---

## Required Inputs (If Available)
Use provided data when present:
- Item name or SKU
- Current stock quantity
- Minimum stock threshold
- Average daily or weekly sales
- Lead time (days)
- Last updated timestamp

If some inputs are missing:
- Make conservative assumptions
- Clearly state assumptions in output

---

## Procedure
1. Identify the inventory event (sale, purchase, return, or check)
2. Apply the stock change accurately
3. Validate stock quantity (no negative values)
4. Compare current stock against minimum threshold
5. Analyze recent sales velocity
6. Estimate days of stock remaining
7. Calculate suggested reorder quantity using:
   - Sales velocity
   - Lead time
   - Safety buffer
8. Generate alerts if risk is detected
9. Summarize inventory status clearly

---

## Reorder Quantity Logic
When suggesting reorder quantities:
- Cover demand for lead time duration
- Add a safety buffer (10–30% if not specified)
- Avoid recommending zero or negative values
- Prefer clarity over complex math explanations

---

## Alert Rules
Trigger alerts when:
- Stock ≤ minimum threshold
- Estimated days of stock < lead time
- Item has no recent restock activity
- Sudden sales spike causes rapid depletion

Alert severity:
- **Critical**: Immediate stockout risk
- **Warning**: Low stock, reorder soon
- **Info**: Stock healthy but trending down

---

## Output Format

### Stock Update Confirmation
- Item
- Event Type (Sale / Purchase / Return)
- Quantity Changed
- Current Stock
- Last Updated Timestamp

### Low Stock Alerts
- Item
- Current Stock
- Minimum Threshold
- Estimated Days Remaining
- Alert Severity

### Reorder Suggestions
- Item
- Suggested Reorder Quantity
- Reasoning (sales trend, lead time, buffer)
- Priority Level

### Inventory Summary (Optional)
- Item
- Current Stock
- Stock Status (Healthy / Low / Critical)
- Last Updated

---

## Tone and Style Guidelines
- Be concise and business-focused
- Use bullet points and structured sections
- Avoid unnecessary technical jargon
- Clearly separate alerts from normal updates
- Prioritize actionable information

---

## Assumptions Handling
If data is missing:
- State assumptions explicitly
- Avoid false precision
- Encourage user to provide missing values

Example:
> "Assuming average sales of 5 units/day due to missing sales history."

---

## Error Handling
If inventory data is inconsistent:
- Flag the issue clearly
- Do not guess silently
- Suggest corrective action

---

## Goal
Help the user:
- Avoid stockouts
- Reduce excess inventory
- Make informed purchasing decisions
- Maintain inventory accuracy with minimal effort

This skill should feel like a vigilant inventory assistant that never sleeps.
