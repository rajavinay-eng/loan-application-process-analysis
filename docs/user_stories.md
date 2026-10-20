# User stories

Each story links back to a requirement in the BRD (BR-01 to BR-06).

---

### US-01: Offer reminders (BR-01)

As a customer who has received a loan offer, I want a reminder before it expires, so that I don't lose the offer by forgetting about it.

**Acceptance criteria**
- Given an offer was sent and the customer hasn't replied, when 7 days have passed, then the customer gets a reminder by email and SMS.
- Given there's still no reply, when 14 days have passed, then a second reminder is sent saying how many days are left.
- Given the customer has already replied, then no reminder is sent.

---

### US-02: Document checklist at the start (BR-02)

As a customer applying for a loan, I want to see the full list of documents I'll need before I submit, so that I can get everything ready at once.

**Acceptance criteria**
- Given a customer opens the application form, when they choose a loan type, then the matching document checklist is shown.
- Given the checklist is shown, then it can be downloaded or emailed to the customer.

---

### US-03: See what's missing (BR-03)

As a customer, I want to upload my documents and see which ones are still missing, so that I don't have to wait for the bank to tell me.

**Acceptance criteria**
- Given a customer has uploaded some documents, when they open their application, then they see each required document marked as received or missing.
- Given a document is rejected, then the customer sees the reason and can upload a new one.

---

### US-04: Fewer document chases for loan officers (BR-02, BR-03)

As a loan officer, I want to see at a glance which documents are missing, so that I don't have to send applications back more than once.

**Acceptance criteria**
- Given an application is in validation, when I open it, then I see a list of missing or rejected documents.
- Given I mark an application as incomplete, then the customer is told exactly which documents are needed in a single message.

---

### US-05: Follow-up for online applicants (BR-04)

As a customer service agent, I want a list of online applicants who received an offer but haven't replied within 5 days, so that I can call them and answer questions.

**Acceptance criteria**
- Given an online application has an offer with no reply after 5 days, then it appears on the agent's follow-up list.
- Given the agent has contacted the customer, then they can log the outcome and the case leaves the list.

---

### US-06: Process dashboard (BR-05)

As the head of lending operations, I want a dashboard showing approval rate, cancellation rate and waiting time by step, so that I can spot problems early.

**Acceptance criteria**
- Given I open the dashboard, then I see approval rate, cancellation rate, median days to outcome and total applications.
- Given I filter by channel or month, then all figures update together.
- Given the data is refreshed, then the dashboard shows the date of the last refresh.

---

### US-07: Workload view (BR-06)

As a team manager, I want to see how many tasks each staff member completes each week, so that I can balance the workload.

**Acceptance criteria**
- Given I open the workload report, then I see completed tasks per person for the selected week.
- Given the system account (User_1) exists, then it's excluded from the report.