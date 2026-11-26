# Registration Form — Field Plan

**Page:** `HTML/register.html`
**Form method:** `GET` (the page explains that this is used to demonstrate submitted `name=value` pairs).

| Field / label | Control | `name` and submitted value | Validation attributes currently present | Reason for each attribute / rule |
|---|---|---|---|---|
| Full name | `input type="text"` | `student_name` | `required`, `minlength="2"`, `maxlength="80"` | Required because a registration needs an identifying name; minimum length rejects a one-character entry; maximum length limits the value to a practical 80 characters. |
| Email address | `input type="email"` | `student_email` | `required` | Required to provide a contact address; email type enables the browser's built-in email-format check. |
| Preferred date | `input type="date"` | `session_date` | `required` | Required because the registration needs a requested session date; date type provides a date control and date-format validation. |
| Preferred start time | `input type="time"` | `session_time` | `required` | Required because the form asks for a preferred start time; time type provides a time control and time-format validation. |
| Number of attendees | `input type="number"` | `participant_count` | `min="1"`, `max="5"`, `step="1"` | Optional field; minimum and maximum constrain the count to 1–5, and step 1 allows whole-number attendee counts. |
| Preferred session topic | Radio group | `session_type` with values `process-models`, `agile`, or `requirements` | `required` on the first radio in the group | Makes selection of one session topic mandatory; radios sharing a name form one mutually exclusive group. Verify native group validation in the browsers tested. |
| Topics of interest | Checkbox group | `topic` with values `software-quality`, `process-models`, `agile`, `agile-tools`, `requirements`, `software-testing` | No validation attributes | Optional multi-select preferences; the current form does not require any checkbox to be selected. Unchecked checkboxes are not submitted. |
| Project or portfolio URL | `input type="url"` | `project_url` | No validation attributes | Optional field; URL type provides browser format checking when a value is entered. |

## Additional form controls

| Control | Type | Purpose |
|---|---|---|
| Submit | `button type="submit"` | Submits the form using GET. |
| Reset | `button type="reset"` | Resets controls to their initial values. |
| Help | `button type="button"` with `popovertarget` | Opens the native registration-help popover; it does not submit the form. |

## Grouping and labels

- The form uses `fieldset` and `legend` to group related controls.
- Every input has a corresponding `label[for]` whose `for` value matches the input `id`.
- The radio buttons share the `session_type` name; checkboxes share the `topic` name.
- Eight distinct input types are present: `text`, `email`, `date`, `time`, `number`, `radio`, `checkbox`, and `url`.

## Data minimisation

The current form asks for name, email, date, time, attendee count, selected session, optional interests, and an optional project URL. It does not ask for unrelated personal information. The assignment reflection should explain which data was deliberately not collected and why.

**Testing note:** This is a plan based on the source code. Actual browser validation behaviour and submitted query parameters must be recorded in the evidence files; they are not assumed here.
