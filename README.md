# ReadyDoor 🚪

> An application-readiness tool for affordable housing

Built for the Hack-Nation Global AI Hackathon 2026 — RealPage Challenge.

## What is ReadyDoor?

Applying for affordable housing can become difficult because of simple documentation problems. A document may be expired, a required file may be missing, or information may be misunderstood.

ReadyDoor helps renters find and fix these problems before their application is reviewed by a housing officer.

The idea is simple:

**AI extracts information → the renter checks it → the system applies the rules → a human makes the final decision.**

ReadyDoor does not decide whether someone is eligible for housing.

For this MVP, the system uses the 2026 HUD MTSP Income Limits for the LIHTC 60% AMI program in Cambridge, Massachusetts.

## What ReadyDoor Does

### 1. Document Extraction and Evidence

ReadyDoor extracts useful information from uploaded documents and shows the evidence behind each value.

For example, if the system finds a gross pay of $1,420, the user can see the text used to find that value.

The renter must confirm the information before it is used in the rest of the application.

### 2. Explaining Changes

If the renter changes something like household size from 3 to 4, ReadyDoor shows what changed and how it affects the relevant income threshold.

Instead of silently recalculating in the background, the system explains the change and shows the source of the rule.

### 3. Application Preparation Map

ReadyDoor does not give the renter an eligibility score.

Instead, it organizes the application into four simple states:

- **Confirmed** — information checked by the renter
- **Needs Review** — something still needs attention
- **Missing** — a required document or piece of information is missing
- **Expired** — a document is no longer valid

For missing or expired items, the system explains why the issue matters and what the renter can do next.

## How It Works

```text
Uploaded Documents
        ↓
Document Extraction
        ↓
Evidence Shown to Renter
        ↓
Renter Confirms or Corrects Information
        ↓
Deterministic Rule Calculations
        ↓
Application Preparation Map
        ↓
Packet Preview and Session Deletion
