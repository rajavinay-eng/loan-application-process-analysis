# Process: as-is and to-be

## As-is (2016, from the data)

```mermaid
flowchart LR
    A["Application created"] --> B["Bank checks and accepts"]
    B --> C["Offer sent"]
    C --> D{"Customer replies?"}
    D -->|"No reply for ~30 days"| X["Cancelled"]
    D -->|"Replies"| E["Validation"]
    E -->|"Documents missing"| F["Marked incomplete, bank chases customer"]
    F --> E
    E -->|"Passes"| P["Approved"]
    E -->|"Fails"| N["Denied"]
```

What goes wrong today: after the offer is sent there's no contact, and many offers simply expire. During validation, most applications bounce back at least once because documents are missing.

## To-be (proposed)

```mermaid
flowchart LR
    A0["Customer sees document checklist"] --> A["Application created"]
    A --> B["Bank checks and accepts"]
    B --> C["Offer sent"]
    C --> W{"Customer replied?"}
    W -->|"Day 7, no"| R1["Reminder by email and SMS"]
    R1 --> W
    W -->|"Day 14, no"| R2["Second reminder, call if online applicant"]
    R2 --> W
    W -->|"Day 30, no"| X["Cancelled"]
    W -->|"Yes"| E["Validation"]
    E -->|"Documents missing"| U["Customer sees what's missing and uploads"]
    U --> E
    E -->|"Passes"| P["Approved"]
    E -->|"Fails"| N["Denied"]
```

What changes: customers know what to send before they apply, they're reminded before an offer expires, and they can fix missing documents themselves instead of waiting to be told.