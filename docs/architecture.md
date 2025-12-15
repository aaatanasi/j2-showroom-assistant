# J2 Showroom Assistant Architecture

This project demonstrates a rules-first approach to using GPTs
for operational workflows.

Core principles:
- Schema is authoritative
- Rules override creativity
- No inference of business-critical fields
- Validation before output

Flow:
Appointment Data → Rule-Based Transformation → Schema Validation → CRM Import

## Human-Centered Design

The system is designed to meet users where they are.

Rather than forcing showroom teams to change how they log appointments,
notes, and brand feedback, J2 adapts to existing spreadsheets and habits.
The LLM functions as a translation layer, transforming familiar inputs
into structured CRM data without disrupting day-to-day workflows.

This approach prioritizes adoption, accuracy, and continuity over process redesign.
