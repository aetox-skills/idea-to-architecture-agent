# AI Agent Notes

Status: Proposed handoff notes

## User Intent to Preserve

- User-provided: Tennis court booking system.
- User-provided: Coaches are part of the concept.
- User-provided: Member discounts are part of the concept.
- User-provided: Payments are part of the concept.
- User-provided: Admin management is part of the concept.

## Active Assumptions

- Assumed: Single-venue first version.
- Assumed: Booking can optionally include a coach.
- Requires approval: Payment provider handles payment processing.
- Assumed: Payment success confirms booking.
- Assumed: Admin changes that affect payment, booking, pricing, or availability should be audited.

## Decisions Requiring Approval

- Requires approval: Single-venue versus multi-venue model.
- Requires approval: Payment provider.
- Requires approval: Payment timing and booking hold timeout.
- Requires approval: Refund and cancellation policy.
- Requires approval: Member discount policy.
- Requires approval: Coach booking model.

## Unknowns

- Unknown: Expected booking volume.
- Unknown: Admin permission granularity.
- Unknown: Notification channels.
- Unknown: Tax, receipt, and invoice requirements.
- Unknown: Data retention requirements.

## Do Not Do

- Do not claim this architecture exists.
- Do not switch this raw-idea example into existing-system work.
- Do not generate implementation scaffolding before approval.

## Safe Next Actions

- Review open questions with the business owner.
- Approve or revise the proposed module boundaries.
- Approve payment, refund, and booking lifecycle decisions.
- Convert only approved proposal sections into implementation tasks.
