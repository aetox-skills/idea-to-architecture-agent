# Workflow Proposal

Status: Proposed

## Proposed Workflows

| Workflow | Actor | Trigger | Outcome |
| --- | --- | --- | --- |
| Proposed: court booking with payment | Customer or member | Selects court time | Proposed: booking is confirmed after successful payment. |
| Proposed: court booking with coach add-on | Customer or member | Selects court time and coach | Proposed: booking reserves court and coach after successful payment. |
| Proposed: admin schedule management | Admin | Updates court hours, closures, or coach availability | Proposed: future availability reflects admin changes. |
| Proposed: cancellation and refund review | Customer or admin | Cancels booking | Proposed: booking status changes and refund path follows approved policy. |

## Proposed: Court Booking With Payment

1. Proposed: customer selects date, time, and court.
2. Proposed system checks court availability.
3. Proposed system calculates price and member discount if applicable.
4. Proposed: customer reviews price and booking details.
5. Proposed system creates a temporary booking hold.
6. Requires approval: selected payment provider collects payment.
7. Requires approval: selected payment provider sends payment result.
8. Proposed booking module confirms booking after successful payment.
9. Proposed notification module sends confirmation.

## Proposed: Coach Add-On

1. Proposed: customer selects date, time, court, and coach.
2. Proposed system checks court availability and coach availability.
3. Proposed pricing module calculates court fee, coach fee, and member discount.
4. Requires approval: customer completes payment through the selected payment provider.
5. Proposed booking module confirms court and coach reservation together.

## Failure Paths

| Failure | Proposed handling | Open question |
| --- | --- | --- |
| Payment fails | Proposed: release temporary booking hold and notify customer. | Unknown: hold duration before release. |
| Selected payment provider event is delayed | Proposed: keep booking in pending payment state until timeout or reconciliation. | Requires approval: timeout policy. |
| Coach becomes unavailable | Proposed: prevent confirmation or require admin/manual resolution. | Unknown: coach override rules. |
| Admin changes court availability after booking | Proposed: preserve confirmed bookings unless admin explicitly cancels. | Requires approval: compensation/refund policy. |
