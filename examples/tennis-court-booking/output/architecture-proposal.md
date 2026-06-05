# Architecture Proposal

Status: Proposed

## User-Provided Intent

User-provided: Create a tennis court booking system with coaches, member
discounts, payments, and admin management.

## Assumptions

| Assumption | Impact if wrong | Requires approval |
| --- | --- | --- |
| Assumed: The first version serves one tennis venue. | Multi-venue support adds tenancy, venue-specific pricing, and admin partitioning. | Yes |
| Assumed: A booking can optionally include a coach. | If coach booking is separate, workflow and pricing boundaries change. | Yes |
| Assumed: Payment processing will use an approval-selected provider. | Provider choice changes integration, webhooks, refunds, and compliance scope. | Yes |
| Assumed: Admins need basic audit history for booking and payment-impacting changes. | Without audit needs, data model can be simpler. | No |

## Proposed Architecture Summary

Proposed: Use a modular application boundary with shared identity, booking,
availability, coach scheduling, pricing/discounts, payments, admin, and
notification responsibilities.

Proposed: Keep modules in one deployable application for the first version
unless scale, team ownership, or compliance requirements justify service
separation later.

## Proposed Modules

| Module | Proposed responsibility | Boundary notes |
| --- | --- | --- |
| Identity and Access | Proposed: manage customer, member, coach, and admin access. | Requires approval for role rules and admin permissions. |
| Court Inventory | Proposed: manage courts, operating hours, closures, and maintenance blocks. | Proposed boundary: owns court availability inputs, not paid booking state. |
| Coach Scheduling | Proposed: manage coach profiles and availability. | Unknown whether coaches are booked standalone or only as add-ons. |
| Booking | Proposed: coordinate reservation lifecycle and availability holds. | Proposed boundary: owns booking states and conflict prevention. |
| Pricing and Discounts | Proposed: calculate court price, coach price, and member discounts. | Requires approval for discount rules. |
| Payments | Proposed: create payment sessions, receive provider events, and update booking payment status. | Provider choice is unknown and requires approval. |
| Admin Management | Proposed: expose operational controls for schedules, pricing, users, and exceptions. | Proposed boundary: records audit events for payment-impacting changes. |
| Notifications | Proposed: send booking confirmations, payment updates, and cancellation messages. | Unknown: notification channel choice. |

## Proposed Integrations

| Integration | Proposed purpose | Decision status |
| --- | --- | --- |
| Payment provider | Requires approval: process card or digital payments through an approved provider. | Requires approval |
| Email or messaging provider | Proposed: send booking and payment notifications. | Unknown |
| Calendar integration | Proposed: optional coach or customer calendar sync. | Deferred |

## Decisions Requiring Approval

Note: This example keeps decision options inside the proposal to avoid unnecessary files.

| Decision | Options | Recommendation |
| --- | --- | --- |
| Venue model | Single venue, multi-venue, marketplace | Proposed: single venue first. |
| Payment timing | Pay before confirmation, deposit, pay later | Proposed: payment before confirmation. |
| Coach booking model | Add-on to court booking, standalone booking, both | Proposed: optional add-on first. |
| Discount model | Fixed member discount, tiers, campaigns | Proposed: tier-based member discount. |
| Refund policy | Manual refund, automatic rules, provider-supported workflow | Unknown; requires business approval. |

## Unknowns

- Unknown: Expected booking volume and peak concurrency.
- Unknown: Tax, invoice, and refund requirements.
- Unknown: Whether admins need granular role permissions.
- Unknown: Notification channels.

## Safe Next Actions

- Confirm approval-required decisions with the business owner.
- Validate booking and payment lifecycle with a small workflow review.
- Review proposed module boundaries before implementation planning.
