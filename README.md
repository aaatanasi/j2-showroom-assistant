# J2 Showroom Assistant

J2 Showroom Assistant is a GPT-based operations tool designed for fashion showrooms.
It converts appointment spreadsheets into CRM-ready opportunity records using
strict schema enforcement, brand normalization, and validation rules.

The system is intentionally designed as a **translation layer** between existing
human workflows and structured business systems, allowing teams to continue
working in familiar formats while ensuring clean, accurate CRM data.

---

## What It Does

- Converts appointment CSV/XLSX files into CRM-importable Opportunity CSVs
- Enforces strict column order and naming
- Splits a single appointment into multiple opportunities by brand
- Normalizes brand names and prevents duplicates
- Applies event mapping (PARIS, MILAN, FACETIME, SHOWROOM NYC, etc.)
- Requires explicit season input to avoid silent errors
- Refuses to infer or guess missing or ambiguous data

---

## Design Philosophy

This system was intentionally designed to adapt to existing showroom workflows,
not force the showroom to change how they work.

Sales teams continue to track appointments and notes in the same spreadsheet
formats they are already comfortable with.
J2 acts as a translation layer that converts this familiar input into structured,
CRM-ready opportunity records.

By preserving existing habits and introducing structure only at the output stage,
the system reduces friction, improves adoption, and avoids operational disruption.

---

## Voice Modeling Approach

The communication style used by J2 is derived from the established email-writing
patterns of showroom leadership.

Rather than inventing a new tone, the system models an existing voice already used
in daily operations in order to preserve consistency across outreach, follow-ups,
and administrative communication.

This approach is intended for internal operational use and brand continuity,
not for personal representation or identity replication.

---

## Architecture

The system is built around three core knowledge files, each with a single responsibility:

### 1. Voice Pack
Defines tone and communication behavior for showroom emails and messaging.
The voice is modeled after existing showroom leadership communication to ensure
continuity and consistency.

### 2. Opportunity Template Schema
Defines the exact CRM contract:
- column names
- column order
- allowed brand values
- formatting and normalization rules

This schema is authoritative and prevents malformed imports.

### 3. Opportunity Output Rules
Defines transformation logic:
- brand extraction hierarchy
- row splitting by brand
- event name mapping
- opportunity status rules
- validation behavior

Rules override creativity.
The system prioritizes correctness and safety over convenience.

---

## Example Workflow

1. Upload appointment CSV/XLSX (as currently used by the showroom)
2. Provide season (e.g. PFW26)
3. J2 outputs a CRM-ready Opportunity CSV
4. CSV is imported directly into the CRM

See the `/examples` directory for sample input and output files.

---

## Why This Matters

Many AI projects focus on content generation alone.
This project focuses on operational reality:

- respecting existing human workflows
- enforcing data integrity
- preventing AI hallucinations
- supporting real-world adoption

It demonstrates how AI can be introduced without requiring teams
to relearn or abandon systems they already trust.

---
