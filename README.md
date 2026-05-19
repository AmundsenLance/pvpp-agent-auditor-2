# PV-PP Agent Auditor Demo Page

This repository contains a standalone test page for the PV-PP Agent Auditor demo flow.

The page is designed to support an interactive fictional-company audit demo using **Northbridge**, a sample organization with fictional agent materials. The goal is to let users experience the audit workflow without needing to upload proprietary company data during first contact.

## Purpose

Many organizations will hesitate to upload real internal materials, prompts, workflows, policies, customer data, or control documents into a new audit tool just to test it.

This demo page solves that problem by giving users a safe, fictional audit environment where they can:

1. Read about the PV-PP Agent Auditor.
2. Download sample Northbridge files.
3. Re-upload those files into the auditor.
4. Run through the audit intake process.
5. Generate or compare against a sample audit report.

## Current Status

This is an early test page.

The current `index.html` includes:

- Main hero section
- Auditor description
- Northbridge interactive demo section
- Placeholder download buttons
- Placeholder sample report button
- Link to the live PV-PP Agent Auditor GPT
- Link back to the main research hub

Some buttons currently use `href="#"` or placeholder styling. These should be wired after the sample materials and generated report pages are created.

## Intended User Flow

1. User lands on the PV-PP Agent Auditor demo page.
2. User reads why a fictional demo case is provided.
3. User downloads the Northbridge sample files.
4. User opens the PV-PP Agent Auditor.
5. User uploads the Northbridge files.
6. User asks the auditor to run the audit.
7. User answers any remaining intake questions.
8. User receives a PV-PP Agent Audit Report.
9. User compares their generated report with the expected sample output.

## Planned Demo Files

The page currently anticipates files such as:

- Northbridge Agent Overview
- Tool & Permission Rules
- Escalation SOP
- Sample Cases
- Full Demo Pack

These files should be fictional and should not contain real company, customer, legal, financial, medical, or security data.

## Recommended Repository Structure

```text
/
├── index.html
├── README.md
├── downloads/
│   ├── northbridge-agent-overview.pdf
│   ├── northbridge-tool-permission-rules.pdf
│   ├── northbridge-escalation-sop.pdf
│   ├── northbridge-sample-cases.pdf
│   └── northbridge-demo-pack.zip
└── reports/
    └── northbridge-generated-sample-report.html
```

## Notes for Future Updates

Before replacing the live auditor page, test that:

- All download links work.
- The auditor GPT link opens correctly.
- The sample files upload cleanly.
- The auditor can extract useful facts from the files.
- The generated report is consistent enough to serve as a public demo.
- The page is readable on mobile.
- Placeholder buttons have been removed or clearly marked.

## Limits

The Northbridge demo is fictional. It is intended for product demonstration, onboarding, and workflow testing.

The PV-PP Agent Auditor does not certify AI systems as safe, compliant, secure, or production-ready. It provides a structured risk interpretation based on supplied information.
