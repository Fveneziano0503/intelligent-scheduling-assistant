# High-Level Architecture Notes

This document describes a proposed architecture, not verified live connections. It intentionally remains implementation-agnostic.

## Conceptual Layers

1. **Calendar Sources**
   - Microsoft 365 / Outlook
   - Google Calendar
   - iCloud / CalDAV or other supported sources

2. **Calendar Connectivity Layer**
   - Retrieves authorized event and availability context
   - Normalizes scheduling information for downstream review

3. **Scheduling Context**
   - Availability
   - Existing events
   - Working hours
   - Transition buffers
   - Focus blocks
   - Meeting preferences

4. **Decision Support**
   - Conflict detection
   - Constraint review
   - Alternative time generation
   - Natural-language scheduling assistance

5. **Human Approval**
   - Review proposed scheduling actions
   - Confirm or reject consequential changes

6. **Calendar Action**
   - Final action occurs only through an authorized provider workflow

## Intentionally Excluded from Public Documentation

- Authentication implementation
- Provider secrets
- Prompt design
- Tool schemas
- Ranking algorithms
- Scheduling heuristics
- Production deployment architecture
- Customer-specific logic
