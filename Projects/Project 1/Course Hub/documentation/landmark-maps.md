# Landmark Maps — Accessible Course Mini-Site

**Source reviewed:** current `HTML/*.html` files.

> These maps document the current implementation. The assignment specifies that plans should be prepared before coding. Enter the real planning/documentation date; do not backdate this document.

## Shared structure (all four pages)

- **Banner:** site header (`header.site-header`).
  - **Navigation:** `nav[aria-label="Main navigation"]`.
- **Main:** `main#main-content`.
- **Contentinfo:** site footer (`footer.site-footer`).
- A **Complementary** landmark is provided by the page-specific `aside` on the Home and Staff pages.

## `index.html` — Course Home

```text
Banner: CSD341 | Software Engineering
└── Navigation: Main navigation
Main: Software Engineering Course
├── About the Course [named section]
├── Learning Outcomes [named section]
├── Course Content [named section]
├── A Software Process at a Glance [named section]
├── Key Course Terms [named section]
└── Learning Resources [named section]
Complementary: A Note About the Lecture Set
Contentinfo: Site footer
```

## `staff.html` — Course Staff

```text
Banner: CSD341 | Software Engineering
└── Navigation: Main navigation
Main: Course Staff and Student Support
├── Teaching Roles [named section]
├── Course Instructor [named section]
├── Practical and Laboratory Support [named section]
├── What Can You Ask About? [named section]
├── How to Ask for Help [named section]
└── Related Course Pages [named section]
Complementary: Before Contacting the Teaching Team
Contentinfo: Site footer
```

## `schedule.html` — Course Schedule

```text
Banner: CSD341 | Software Engineering
└── Navigation: Main navigation
Main: Course Topic Schedule
├── Lecture-by-Lecture Plan [named section]
└── Schedule Notes [named section]
Contentinfo: Site footer
```

## `register.html` — Registration

```text
Banner: CSD341 | Software Engineering
└── Navigation: Main navigation
Main: Workshop and Practical Session Registration
├── Registration form (not currently named as a landmark)
├── Form Guidance (popover content; not a page landmark)
└── Data and Submission Method [named section]
Contentinfo: Site footer
```

**Note:** The `aside` elements on Home and Staff have accessible names through `aria-labelledby`. The sections shown as named are sections with `aria-labelledby`; their exposure as Region landmarks depends on their accessible names and browser/screen-reader behaviour. Confirm the actual announced landmark list during the screen-reader test. The registration form currently has no accessible name, so this plan does not count it as a named Form landmark.
