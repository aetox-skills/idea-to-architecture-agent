# Module Proposal

Status: Proposed

## Proposed Module Boundaries

| Module | Proposed responsibilities | Proposed exclusions | Open questions |
| --- | --- | --- | --- |
| Identity and Access | Proposed: accounts, roles, session access, member status visibility. | Proposed exclusion: discount calculation. | Unknown: admin role granularity. |
| Court Inventory | Proposed: courts, operating hours, blackout periods, maintenance. | Proposed exclusion: payment ownership. | Unknown: one venue or many. |
| Coach Scheduling | Proposed: coach profiles, availability, booking eligibility. | Proposed exclusion: court pricing. | Unknown: standalone coach booking. |
| Booking | Proposed: booking requests, availability holds, status transitions, cancellation requests. | Proposed exclusion: payment method processing. | Requires approval: hold duration before payment. |
| Pricing and Discounts | Proposed: base rates, coach fees, member discounts, pricing explanations. | Proposed exclusion: booking confirmation. | Unknown: discount policy. |
| Payments | Proposed: payment session creation, provider event handling, payment status. | Proposed exclusion: raw card data storage. | Requires approval: provider and refund policy. |
| Admin Management | Proposed: admin screens and actions for operations and exceptions. | Proposed exclusion: unaudited payment-impacting changes. | Unknown: audit depth. |
| Notifications | Proposed: confirmation, cancellation, payment status messages. | Proposed exclusion: booking state decisions. | Unknown: email, SMS, or in-app only. |

## Proposed Shared Concerns

| Concern | Proposed owner | Notes |
| --- | --- | --- |
| Authorization | Proposed: Identity and Access | Proposed: role checks for admin, coach, member, customer. |
| Audit events | Proposed: Admin Management | Proposed: capture pricing, booking, refund, and schedule changes. |
| Pricing consistency | Proposed: Pricing and Discounts | Proposed: booking stores quoted price snapshot. |
| Payment state reconciliation | Proposed: Payments | Proposed: provider webhook updates booking payment status. |

## Approval Points

- Requires approval: Whether first version is single-venue.
- Requires approval: Payment provider and payment timing.
- Requires approval: Refund and cancellation policy.
- Requires approval: Coach booking model.
