# UAT test cases

These test the features in the user stories. "Result" stays empty until testing happens. I've included a few edge cases on purpose, because that's usually where things break.

| ID | Story | Scenario | Steps | Expected result | Result |
|---|---|---|---|---|---|
| UAT-01 | US-01 | First reminder is sent | Create an offer. Don't reply. Move the test clock forward 7 days. | Customer gets one email and one SMS reminder. | |
| UAT-02 | US-01 | Second reminder is sent | Same offer, still no reply. Move the clock to day 14. | Second reminder arrives and shows days left. | |
| UAT-03 | US-01 | No reminder after reply | Create an offer. Customer replies on day 3. Move clock to day 7. | No reminder is sent. | |
| UAT-04 | US-01 | Reply on the same day as the reminder | Customer replies on day 7, an hour before the reminder runs. | No reminder is sent. | |
| UAT-05 | US-01 | Offer expires | No reply. Move clock to day 30. | Application is cancelled. No further reminders. | |
| UAT-06 | US-02 | Checklist matches loan type | Start an application, pick "Car". Then start another and pick "Home improvement". | Each shows the correct document list for that loan type. | |
| UAT-07 | US-03 | Missing documents shown | Upload 2 of 4 required documents. Open the application. | 2 marked received, 2 marked missing. | |
| UAT-08 | US-03 | Rejected document | Loan officer rejects one document with a reason. | Customer sees the reason and can upload a new file. | |
| UAT-09 | US-05 | Online applicant appears on follow-up list | Online application, offer sent, no reply for 5 days. | Appears on the agent's list. Staff-entered applications don't. | |
| UAT-10 | US-06 | Dashboard numbers are correct | Compare dashboard figures with a direct count from the source data. | Totals and rates match exactly. | |
| UAT-11 | US-06 | Filters update everything | Filter the dashboard to "Online" only. | All cards and charts change together. | |
| UAT-12 | US-07 | System user excluded | Open the workload report. | User_1 does not appear. | |

## How I checked UAT-10 in this project

I did a version of this myself. The Power BI cards matched my Python results: 54.85% approval (17,228 of 31,411 finished applications), 33.21% cancellation and a median of about 19.1 days.