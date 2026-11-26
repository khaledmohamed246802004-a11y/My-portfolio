# Network Evidence — Submitted `name=value` Pairs

**Page:** `register.html`  
**Form method:** `GET`  
**Test:** The user submitted fictional test data in Safari and confirmed that the submitted field names and values appeared in the address bar after the `?` query-string separator. This confirms that the GET form submission serializes successful named controls as query parameters. The exact test values were not supplied for this record, so they are intentionally not reproduced.

| Control | Expected key | Submission behaviour | Observed result |
|---|---|---|---|
| Full name | `student_name` | Sent when the named control has a value | Query string appeared after submission; Pass |
| Email address | `student_email` | Sent when the named control has a value | Query string appeared after submission; Pass |
| Preferred date | `session_date` | Sent when the named control has a value | Query string appeared after submission; Pass |
| Preferred start time | `session_time` | Sent when the named control has a value | Query string appeared after submission; Pass |
| Number of attendees | `participant_count` | Optional; sent when a value is provided | GET query string observed; exact optional-field serialization not separately recorded |
| Preferred session | `session_type` | Only the selected radio value is sent | GET query string observed; individual value not transcribed |
| Topics of interest | `topic` | Each checked checkbox contributes a value; unchecked boxes are omitted | GET query string observed; individual values not transcribed |
| Project URL | `project_url` | Optional; sent when a value is provided | GET query string observed; exact value not transcribed |

## Explanation

A GET form appends successful controls to the page URL as a query string. Each parameter uses the control's `name` as the key and its entered or selected value as the value, in the general form `name=value`. Parameters are separated by `&`; characters that need encoding are percent-encoded. Controls without a `name`, unchecked checkboxes, and unselected radio buttons are not submitted. Because GET data is visible in the URL and may be stored in browser history or logs, this demonstration uses fictional data only and must not be used for confidential information.

**Result:** GET query-string visibility — **Pass** (user-confirmed). Exact values and a Network-panel screenshot were not provided; no values or screenshots have been invented.
