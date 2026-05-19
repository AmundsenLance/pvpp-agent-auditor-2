# Northbridge Demo — Tool and Permission Rules

**Document status:** Fictional demo material for the PV-PP Agent Auditor  
**Company:** Northbridge Office Supply & Services  
**Agent:** Northbridge Invoice Exception Assistant  
**Version:** Demo v0.1

---

## 1. Purpose of This File

This file describes the fictional tools, systems, data sources, and permission limits available to the Northbridge Invoice Exception Assistant.

The agent is intended to help Accounts Receivable staff review invoice exceptions, but it should remain advisory. It should not execute financial actions or silently change authoritative records.

---

## 2. Available Information Sources

The agent may read from the following sources.

### 2.1 Invoice Exception Queue

Contains:

- Invoice number
- Customer name
- Customer account ID
- Invoice amount
- Exception reason
- Current queue status
- Aging in days
- Assigned staff member
- Prior status labels
- Free-text notes

Known weakness:

- Notes may be incomplete or written in shorthand.
- Prior labels may not reflect the actual evidence reviewed.

---

### 2.2 Customer Account Database

Contains:

- Account status
- Billing address
- Contract tier
- Assigned account manager
- Payment history summary
- Open disputes flag
- Credit hold flag

Known weakness:

- Open dispute details are stored in a separate dispute system.
- Account status may lag behind recent customer communications.

---

### 2.3 Document Repository

Contains:

- Purchase orders
- Signed contracts
- Delivery confirmations
- Service completion records
- Pricing amendments
- Customer emails saved by staff

Known weakness:

- Some documents are scanned PDFs.
- The agent may not reliably extract handwriting, stamps, signatures, or small print.
- Document names may be misleading.
- A document being present does not mean it supports the invoice.

---

### 2.4 Customer Contact Notes

Contains:

- Calls made by billing or customer support
- Email summaries
- Callback notes
- Contact attempts
- Customer acknowledgments

Known weakness:

- "Called customer" may mean contact attempted, not confirmation received.
- "Customer aware" may not identify who confirmed, when, or what was confirmed.
- Notes may not show whether the contact had authority to approve billing.

---

### 2.5 Dispute History System

Contains:

- Prior invoice disputes
- Reasons for prior reversals
- Supervisor comments
- Customer complaints
- Prior credits or corrections

Known weakness:

- The agent can search this system only when the case is already flagged as disputed.
- Some repeat-dispute patterns may be missed if the current case is not flagged.

---

## 3. Agent Permissions

The agent may:

- Read invoice exception records.
- Read customer account summaries.
- Read supporting documents.
- Read customer-contact notes.
- Search dispute history when available.
- Generate a short evidence summary.
- Recommend one workflow label.
- Suggest missing evidence.
- Suggest escalation.

The agent may not:

- Approve an invoice.
- Send an invoice.
- Issue a credit.
- Modify customer master data.
- Close a dispute.
- Change payment terms.
- Write directly to the accounting ledger.
- Send customer communications without human review.
- Mark a human review as complete.

---

## 4. Workflow Labels and Authority Limits

The agent's labels are supposed to be recommendations only.

However, Northbridge staff sometimes use labels as queue filters. Cases marked **Ready for Billing Review** may receive faster and lighter review, especially when the exception queue is backlogged.

This creates a hidden authority risk: the agent may not formally approve billing, but its status label may change the intensity of human review.

---

## 5. Evidence Requirements by Recommendation

### Ready for Billing Review

Minimum expected evidence:

- Invoice matches customer account.
- Purchase order or contract support is present.
- Amount is consistent with support.
- Delivery or service completion evidence exists.
- No unresolved dispute flag.
- No credit hold or billing block.
- Customer-contact notes do not contradict the invoice.

If any of these are missing or uncertain, the agent should not recommend Ready for Billing Review.

---

### Needs Documentation

Use when:

- Required support is missing.
- Document text is unreadable or ambiguous.
- Purchase order does not match invoice amount.
- Delivery or service completion evidence is missing.
- Contract amendment is referenced but not found.

---

### Customer Contact Required

Use when:

- Customer authorization is unclear.
- Customer previously disputed similar charges.
- Notes show attempted contact but not confirmation.
- Service completion is disputed.
- Delivery acceptance is unclear.

---

### Escalate to Supervisor

Use when:

- Invoice amount is above $25,000 and support is incomplete.
- There is a repeat dispute pattern.
- Staff notes conflict with documents.
- Customer authority is unclear.
- The agent cannot determine whether a billing block applies.
- The case involves a strategic customer or threatened complaint.

---

### Do Not Advance

Use when:

- There is an active credit hold.
- There is an unresolved billing block.
- There is a known incorrect customer account.
- The support documents contradict the invoice.
- The agent cannot identify the correct customer or contract.

---

## 6. Logging Requirements

For every recommendation, the agent should provide:

- Recommended label
- Short reason
- Evidence cited
- Missing evidence, if any
- Confidence limitation
- Whether human review is required
- Whether escalation is recommended

Known weakness:

The current workflow captures the agent summary, but it does not consistently capture which source documents were actually opened by the human reviewer.

---

## 7. Known Permission-Risk Issues

The highest-risk permission issue is not that the agent can directly execute financial changes. It cannot.

The higher-risk issue is practical reliance:

- Staff may treat agent summaries as evidence.
- A "Ready" label may reduce review intensity.
- Queue metrics may reward fast movement.
- Errors may be discovered later in disputes, credits, or audit findings.
- Later corrections are not consistently tied back to the original agent label.

---

## 8. Suggested Auditor Focus

When auditing this environment, look closely at:

- Authority boundary integrity
- Evidence sufficiency
- Stale or incomplete data
- Human-review realism
- Label strength
- Metric-capture risk
- Recovery after incorrect advancement
- Whether advisory output becomes operational control
