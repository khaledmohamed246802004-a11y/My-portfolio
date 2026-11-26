# Registration Form — Test Cases

Use fictional data only. The observations below were reported by the user while testing in Google Chrome on 26 November 2026. All listed cases are marked Pass based on the user's confirmation that the full test set was completed successfully in Chrome and Safari. This is user-reported test evidence, not an independent automated browser run.

| # | Browser | Field / scenario | Test input / action | Expected result | Actual result | Pass / Fail | Defect / fix reference |
|---:|---|---|---|---|---|---|---|
| 1 | Chrome and Safari | All required fields empty | Leave all required fields empty and submit | Browser blocks submission and identifies a required field | Chrome result: Browser blocked submission and requested the name. User also confirmed Pass in Safari | Pass | — |
| 2 | Chrome and Safari | Name below minimum length | Enter `A` | Name control is invalid because minlength is 2 | Chrome result: Browser rejected the one-character name. User also confirmed Pass in Safari | Pass | — |
| 3 | Chrome and Safari | Name at minimum length | Enter `Al` | Name control is valid | Chrome result: Accepted; browser proceeded to email. User also confirmed Pass in Safari | Pass | — |
| 4 | Chrome and Safari | Name at maximum length | Enter exactly 80 characters | Name control is valid | Chrome result: User reported that the 80-character name was accepted. User also confirmed Pass in Safari | Pass | — |
| 5 | Chrome and Safari | Name above maximum length | Attempt to enter more than 80 characters | Input cannot exceed 80 characters | Chrome result: Browser stopped accepting further characters. User also confirmed Pass in Safari | Pass | — |
| 6 | Chrome and Safari | Invalid email | Enter `student@` | Email control is invalid | Chrome result: Browser rejected the email. User also confirmed Pass in Safari | Pass | — |
| 7 | Chrome and Safari | Valid email | Enter `student@example.com` | Email control is valid | Chrome result: Accepted; browser proceeded to the next required field. User also confirmed Pass in Safari | Pass | — |
| 8 | Chrome and Safari | Required date empty | Leave preferred date empty | Form validation blocks submission | Chrome result: User confirmed that the required-date validation test passed in Chrome. User also confirmed Pass in Safari | Pass | — |
| 9 | Chrome and Safari | Required time empty | Leave preferred time empty | Form validation blocks submission | Chrome result: Browser rejected submission and required the time. User also confirmed Pass in Safari | Pass | — |
| 10 | Chrome and Safari | Required radio group empty | Do not select a session type | Form validation blocks submission | Chrome result: Browser rejected submission and displayed “Choose one session type (required)”. User also confirmed Pass in Safari | Pass | — |
| 11 | Chrome and Safari | Valid session type and successful submission | Select a session type after completing required fields, then submit | Browser accepts valid form data and submits the GET request | Chrome result: User reported the form submitted successfully. User also confirmed Pass in Safari | Pass | — |
| 12 | Chrome and Safari | Attendee count below minimum | Enter 0 | Number control is invalid | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 13 | Chrome and Safari | Attendee count at minimum | Enter 1 | Number control is valid | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 14 | Chrome and Safari | Attendee count at maximum | Enter 5 | Number control is valid | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 15 | Chrome and Safari | Attendee count above maximum | Enter 6 | Number control is invalid | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 16 | Chrome and Safari | Attendee count non-integer | Enter 2.5 | Number control is invalid because step is 1 | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 17 | Chrome and Safari | No optional interests selected | Leave all topic checkboxes unchecked | Form remains valid; no topic value is submitted | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 18 | Chrome and Safari | Multiple interests selected | Select two topic checkboxes | Both remain checked and both values are submitted | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 19 | Chrome and Safari | Invalid optional URL | Enter `not-a-url` | URL control is invalid | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 20 | Chrome and Safari | Reset button | Change name and select a checkbox, then press Clear form | Values return to their initial defaults | User confirmed this test passed in both Chrome and Safari | Pass | — |
| 21 | Chrome and Safari | Help button | Press Show form guidance | Guidance popover opens and form is not submitted | User confirmed this test passed in both Chrome and Safari | Pass | — |

## Execution notes

- All 21 listed test cases were reported by the user as completed successfully in Google Chrome. The user subsequently confirmed that the tests were also run in Safari and passed.
- The user confirmed successful execution in both Chrome and Safari.
- The form uses GET for classroom demonstration. Submitted values appear in the URL; use fictional values only.
- The successful submission is a browser-side form submission to the same static page. It does not register a real student or contact a university system.
- If a browser behaves differently from the expected result, record the actual behaviour rather than changing the expected result.
