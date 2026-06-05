# Idea Brief

## Raw Idea

User-provided: A tennis court booking system with coaches, member discounts,
payments, and admin management.

## User-Provided Facts

| Fact | Source |
| --- | --- |
| User-provided: Customers can book tennis courts. | Raw idea |
| User-provided: Coaches are part of the concept. | Raw idea |
| User-provided: Member discounts are part of the concept. | Raw idea |
| User-provided: Payments are part of the concept. | Raw idea |
| User-provided: Admin management is part of the concept. | Raw idea |

## Intended Outcomes

- Assumed: Customers can reserve available courts.
- Assumed: Members can receive pricing benefits.
- Assumed: Admins can manage courts, schedules, coaches, members, and bookings.
- Assumed: Payments support booking confirmation.

## Actors

| Actor | Label | Notes |
| --- | --- | --- |
| Customer | Assumed | Books courts and may pay online. |
| Member | User-provided | Receives discounts; exact membership rules are unknown. |
| Coach | User-provided | May be booked with a court or scheduled separately. |
| Admin | User-provided | Manages operational data and exceptions. |

## Architecture-Impacting Questions

| Question | Why it matters | Status |
| --- | --- | --- |
| Is this for one venue, multiple venues, or a marketplace? | Changes tenancy, scheduling, admin scope, and reporting. | Unknown |
| Should coaches be booked independently or only with courts? | Changes availability rules and data model. | Unknown |
| Which payment provider and refund policy should be used? | Changes integration, settlement, and failure handling. | Requires approval |
| Are member discounts fixed, tiered, time-based, or promotional? | Changes pricing rules and audit needs. | Unknown |
| Should unpaid bookings temporarily hold court availability? | Changes booking workflow and concurrency handling. | Requires approval |

## Assumptions

| Assumption | Why safe for now | Impact if wrong | Requires approval |
| --- | --- | --- | --- |
| Assumed: First proposal targets a single venue. | Keeps the first architecture lean. | Multi-venue support would add tenancy and venue-level admin boundaries. | Yes |
| Assumed: Online payment confirms a booking. | Common booking pattern. | Pay-later or deposit-only policies would change workflow states. | Yes |
| Assumed: Coaches have availability schedules. | Needed to reason about coach booking. | If coaches are only informational, the coach module can be smaller. | No |
