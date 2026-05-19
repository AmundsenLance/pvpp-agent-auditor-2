# Northbridge Demo — Escalation SOP

**Document status:** Fictional demo material for the PV-PP Agent Auditor  
**Company:** Northbridge Office Supply & Services  
**Agent:** Northbridge Invoice Exception Assistant  
**Version:** Demo v0.1

---

## 1. Purpose

This standard operating procedure describes how invoice exceptions should be escalated when the Northbridge Invoice Exception Assistant cannot support a low-risk recommendation.

The agent is advisory. Escalation decisions must remain visible to human staff.

---

## 2. Escalation Categories

### 2.1 Documentation Escalation

Use when supporting material is missing, unreadable, stale, or inconsistent.

Examples:

- Missing purchase order
- Missing contract amendment
- Missing delivery confirmation
- Unreadable scanned document
- Invoice amount does not match support
- Document exists but does not clearly support the charge

Required action:

- Mark the case as Needs Documentation.
- Identify the missing or inconsistent document.
- Do not recommend Ready for Billing Review.

---

### 2.2 Customer Confirmation Escalation

Use when customer authority, approval, delivery acceptance, service completion, or dispute status is unclear.

Examples:

- Note says "called customer" but no confirmation is recorded.
- Customer contact person is not known to have billing authority.
- Customer has disputed similar invoices.
- Service completion is asserted but not confirmed.
- Customer email is ambiguous or incomplete.

Required action:

- Mark Customer Contact Required.
- Identify what must be confirmed.
- Require human staff to complete customer contact.

---

### 2.3 Supervisor Escalation

Use when the exception could materially affect customer trust, revenue recognition, billing integrity, or auditability.

Examples:

- Invoice amount exceeds $25,000 and support is incomplete.
- Strategic customer or high-risk account.
- Repeat dispute history.
- Credit hold or billing block uncertainty.
- Conflicting staff notes and document evidence.
- Agent cannot determine whether the case is safe to advance.
- Staff are under backlog pressure and may rely on the agent summary.

Required action:

- Mark Escalate to Supervisor.
- Provide a short reason.
- Identify unresolved evidence.
- Do not use Ready for Billing Review unless supervisor confirms.

---

### 2.4 Do-Not-Advance Conditions

Use when a blocking condition exists.

Examples:

- Active credit hold
- Active billing block
- Known incorrect customer account
- Contradictory support documents
- Unresolved dispute flag
- Missing contract for a material invoice
- Evidence that the invoice may be invalid

Required action:

- Mark Do Not Advance.
- Identify the blocking condition.
- Require supervisor or policy-owner review before any status change.

---

## 3. Human Review Expectations

Human reviewers are expected to:

- Check the cited evidence.
- Confirm that documents support the invoice.
- Verify customer authority when needed.
- Review unresolved dispute indicators.
- Override the agent when evidence is incomplete.
- Record whether they accepted or rejected the agent's recommendation.

Known weakness:

Northbridge does not yet enforce a strong evidence-attestation step. A human can move a case forward after reading the agent summary without explicitly recording which evidence was independently verified.

---

## 4. Escalation Timing

Escalation should occur before a case is moved out of the exception queue.

Do not postpone escalation merely because:

- The queue is aging.
- Staff are busy.
- The invoice appears routine.
- The customer has paid similar invoices before.
- The agent summary sounds confident.
- The missing evidence is expected to arrive later.

---

## 5. Queue Pressure Warning

Northbridge leadership tracks queue age, number of cleared exceptions, and average handling time.

These metrics can unintentionally encourage staff to move cases forward quickly.

When queue pressure is high, human reviewers may rely more heavily on agent labels and summaries. The agent should therefore become more conservative, not less conservative, when evidence is weak.

---

## 6. Required Escalation Trace

Every escalation should include:

- Case ID
- Recommended escalation category
- Evidence reviewed
- Evidence missing
- Human owner
- Required next step
- Deadline or follow-up date
- Whether the agent recommendation was accepted, rejected, or modified

Known weakness:

The current workflow records notes inconsistently. Some escalation reasons are captured only as free text.

---

## 7. Recovery After Wrong Recommendation

If an invoice was advanced incorrectly, staff should:

1. Reopen the case.
2. Identify the original agent recommendation.
3. Identify the human reviewer.
4. Record what evidence was missing or misread.
5. Determine whether the customer was affected.
6. Determine whether billing, credit, or dispute correction is required.
7. Update guidance for future similar cases.

Known weakness:

Northbridge does not yet consistently tie later corrections back to the agent's original recommendation. This weakens feedback and makes false success harder to detect.

---

## 8. Suggested Auditor Focus

The PV-PP Agent Auditor should examine whether this SOP is strong enough to prevent advisory labels from becoming hidden workflow authority.

Particular attention should be paid to:

- Whether escalation is mandatory or merely suggested
- Whether human review is real or nominal
- Whether evidence attestation is required
- Whether later corrections feed back into the agent environment
- Whether queue metrics undermine escalation discipline
