# Question Framework

Ask questions that change architecture decisions. Avoid discovery theater.

## Question Types

| Type | Ask When | Example |
| --- | --- | --- |
| Goal | The outcome is ambiguous. | "Is the priority faster booking, higher utilization, or lower admin effort?" |
| Actor | Users or permissions are unclear. | "Which actor can cancel a paid booking?" |
| Boundary | Ownership could split across modules or services. | "Should payments be owned inside this product or delegated to a payment provider?" |
| Data | Persistence, privacy, or reporting needs are unclear. | "Which customer data must be retained after cancellation?" |
| Workflow | Order of operations affects risk. | "Should payment be authorized before or after court availability is held?" |
| Integration | External systems are likely. | "Does this need calendar, payment, email, or club management integration?" |
| Compliance | Rules may constrain design. | "Are there tax, refund, age, or membership rules that affect booking?" |
| Scale | Capacity changes architecture. | "Is this for one venue, many venues, or a marketplace?" |

## Must-Answer Questions

Treat a question as must-answer when the wrong assumption could:

- Expose sensitive data.
- Break payment or refund behavior.
- Create legal or compliance risk.
- Change tenancy or ownership boundaries.
- Make the proposed architecture materially more expensive.
- Invert the user experience or operating model.

## Safe-to-Assume Questions

Assume and label when:

- The answer only changes naming.
- The answer affects a replaceable integration.
- The answer can be revised before implementation.
- The user requested a first-pass proposal.

## Question Budget

For first pass work, ask up to five architecture-impacting questions. If more
are needed, group the rest under open questions and continue with assumptions
where safe.
