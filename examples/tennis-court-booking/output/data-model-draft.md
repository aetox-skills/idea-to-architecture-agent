# Data Model Draft

Status: Proposed

## Proposed Entities

| Entity | Proposed purpose | Key fields | Sensitive data |
| --- | --- | --- | --- |
| User | Proposed: represent login identity and contact profile. | user_id, name, email, phone, role | Yes |
| MemberProfile | Proposed: represent membership status and discount tier. | member_id, user_id, tier, status, valid_from, valid_until | Yes |
| Court | Proposed: represent bookable court inventory. | court_id, name, surface_type, active | No |
| CourtAvailabilityBlock | Proposed: represent operating hours, closures, or maintenance. | block_id, court_id, start_time, end_time, type | No |
| Coach | Proposed: represent coach profile and booking eligibility. | coach_id, user_id, bio, active | Yes |
| CoachAvailabilityBlock | Proposed: represent coach available or unavailable periods. | block_id, coach_id, start_time, end_time, type | No |
| Booking | Proposed: represent court reservation lifecycle. | booking_id, user_id, court_id, coach_id, start_time, end_time, status | Yes |
| PriceQuote | Proposed: preserve price shown before payment. | quote_id, booking_id, base_price, discount_amount, total_amount, currency | No |
| PaymentRecord | Proposed: represent provider payment state. | payment_id, booking_id, provider, provider_reference, status, amount | Yes |
| AuditEvent | Proposed: record admin and payment-impacting changes. | event_id, actor_id, entity_type, entity_id, action, created_at | Yes |
| Notification | Proposed: track sent or failed notifications. | notification_id, booking_id, channel, status, sent_at | Yes |

## Proposed Relationships

| Relationship | Proposed cardinality | Notes |
| --- | --- | --- |
| User to MemberProfile | Proposed: one to zero-or-one | Assumed: not every customer is a member. |
| User to Booking | Proposed: one to many | Proposed: customer owns bookings. |
| Court to Booking | Proposed: one to many | Proposed: overlapping confirmed bookings must be prevented. |
| Coach to Booking | Proposed: one to many optional | Unknown: coach may be optional. |
| Booking to PriceQuote | Proposed: one to one or many revisions | Requires approval: whether quotes can be recalculated. |
| Booking to PaymentRecord | Proposed: one to many | Proposed: supports retries and refunds. |
| User to AuditEvent | Proposed: one to many | Proposed: actor_id records admin actions. |

## Data Ownership

| Data area | Proposed owner | Approval needed |
| --- | --- | --- |
| Booking lifecycle | Proposed: Booking | Requires approval: status model. |
| Pricing rules | Proposed: Pricing and Discounts | Requires approval: discount policy. |
| Payment references | Proposed: Payments | Requires approval: provider choice. |
| Admin audit trail | Proposed: Admin Management | Assumed: no approval unless retention requirements differ. |

## Retention and Audit Questions

- Unknown: How long payment-related records must be retained.
- Unknown: Whether deleted users must anonymize booking history.
- Unknown: Whether refund decisions require immutable audit records.
