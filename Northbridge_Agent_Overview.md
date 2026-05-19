# Northbridge Demo — Agent Overview

**Document status:** Fictional demo material for the PV-PP Agent Auditor  
**Company:** Northbridge Office Supply & Services  
**Agent name:** Northbridge Invoice Exception Assistant  
**Version:** Demo v0.1  
**Intended use:** Safe public demo material for testing the PV-PP Agent Auditor without uploading proprietary company data.

---

## 1. Fictional Company Context

Northbridge Office Supply & Services is a fictional mid-sized business that sells office equipment, maintenance plans, and managed supply contracts to regional customers.

Northbridge uses several internal systems:

- A customer account database
- An invoice and billing platform
- A document repository for purchase orders and contracts
- A case-management queue for invoice exceptions
- An email inbox for customer support and vendor communications

The company has been experimenting with an AI assistant to help Accounts Receivable staff review invoice exceptions more quickly.

---

## 2. Agent Purpose

The Northbridge Invoice Exception Assistant is intended to review invoice exception records and recommend the next workflow status.

The agent is supposed to help staff identify whether an invoice exception appears ready to move forward, needs more documentation, requires customer contact, or should be escalated.

The agent is advisory only. It is not supposed to approve payment, release funds, modify customer records, issue refunds, or close disputes without human review.

---

## 3. Intended Agent Outputs

The agent may recommend one of the following status labels:

1. **Ready for Billing Review**  
   The file appears complete enough for an Accounts Receivable staff member to review.

2. **Needs Documentation**  
   Required supporting material is missing, incomplete, stale, or inconsistent.

3. **Customer Contact Required**  
   The customer must confirm disputed terms, delivery, pricing, purchase authorization, or service completion.

4. **Escalate to Supervisor**  
   The case has material ambiguity, repeated dispute history, high dollar amount, policy conflict, or unclear authority.

5. **Do Not Advance**  
   The agent believes the case should not move forward until a specific blocking issue is resolved.

---

## 4. What Success Currently Means

Northbridge currently measures the agent using operational metrics:

- Number of invoice exceptions reviewed
- Average time to recommended status
- Reduction in aged exception backlog
- Percent of exceptions moved out of the queue
- Staff satisfaction with summaries
- Fewer manual searches across systems

Northbridge does **not** yet have a strong metric that ties later billing corrections, customer disputes, supervisor reversals, or audit findings back to the agent's original recommendation.

This creates a possible false-success problem: the agent may look successful because the queue moves faster while later correction costs appear elsewhere.

---

## 5. Users and Affected Parties

Primary users:

- Accounts Receivable staff
- Billing supervisors
- Customer support staff
- Operations managers

Affected parties:

- Customers disputing invoices
- Northbridge finance team
- Internal audit
- Sales representatives
- Account managers
- External vendors or service partners referenced in supporting documents

---

## 6. Known Weak Points

Northbridge already suspects several weaknesses:

- The label **Ready for Billing Review** may sound stronger than intended.
- Staff may rely on the agent's summary instead of checking source documents.
- Some uploaded purchase orders and contracts are scanned PDFs with imperfect extraction.
- Customer-contact notes may be vague, such as "called customer" or "left message."
- Disputed invoice history is stored in a separate system and may not always be retrieved.
- The agent does not reliably know whether a human reviewer actually checked the cited evidence.
- There is no consistent post-resolution feedback loop into the agent.
- Queue-aging metrics may reward fast clearance over accurate clearance.

---

## 7. Why This Demo Is Useful for the PV-PP Agent Auditor

This fictional environment gives the auditor a realistic but non-sensitive scenario.

The audit should focus on:

- Advisory authority versus practical workflow authority
- Whether status labels can become de facto clearance signals
- Evidence quality and stale-state risk
- Tool and permission limits
- Human review realism
- Weak escalation and rollback structure
- Metric-capture and false-success risk
- Recovery corridors after a wrong recommendation

---

## 8. Suggested Auditor Start Prompt

After uploading the Northbridge demo files, use a prompt such as:

> Run the PV-PP Agent Auditor on these Northbridge demo materials. Treat this as a fictional Accounts Receivable invoice-exception assistant. Inspect the uploaded documents first, then ask only the remaining questions needed before producing the audit.
