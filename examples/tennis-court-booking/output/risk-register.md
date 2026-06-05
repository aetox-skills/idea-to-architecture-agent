# Risk Register

Status: Proposed

| Risk | Label | Impact | Mitigation | Early validation |
| --- | --- | --- | --- | --- |
| Risk: payment succeeds but booking confirmation fails. | Risk | Customer may pay without a confirmed court. | Proposed: idempotent payment event handling and reconciliation. | Proposed validation: review payment webhook workflow. |
| Risk: two users book the same court time. | Risk | Double booking damages trust and operations. | Proposed: availability holds and conflict checks at confirmation. | Proposed validation: test concurrent booking scenarios before implementation. |
| Risk: member discount rules are ambiguous. | Risk | Incorrect pricing or disputes. | Proposed: require approved discount policy and store price quote snapshots. | Proposed validation: confirm discount rules with business owner. |
| Risk: coach availability conflicts with court availability. | Risk | Coach bookings may be invalid. | Proposed: check both availability sources before payment. | Proposed validation: review coach add-on workflow. |
| Risk: refund policy is not defined. | Risk | Support and finance teams may handle cancellations inconsistently. | Proposed: require refund decision before implementation. | Proposed validation: approve cancellation and refund matrix. |
| Risk: admin actions lack audit trail. | Risk | Hard to investigate pricing, refund, or schedule disputes. | Proposed: audit payment-impacting admin changes. | Proposed validation: decide retention and audit scope. |

## Unknowns

- Unknown: Payment provider and refund capabilities.
- Unknown: Peak usage and booking conflict tolerance.
- Unknown: Legal or tax requirements for receipts.
- Unknown: Notification channels and delivery guarantees.
