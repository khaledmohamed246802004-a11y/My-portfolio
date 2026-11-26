# Colour Contrast Measurements

**Method:** WCAG relative luminance and contrast-ratio formula, calculated from the exact CSS colour values. Thresholds: 4.5:1 for normal text and 3:1 for large text.

| Element / state | Foreground | Background | Text size | Measured ratio | AA threshold | Verdict |
|---|---|---|---|---:|---:|---|
| Body text | `#101928` | `#ffffff` | Normal | 17.62:1 | 4.5:1 | Pass |
| Muted text | `#475569` | `#ffffff` | Normal | 7.58:1 | 4.5:1 | Pass |
| Header navigation link | `#334e49` | `#cbdad7` | Normal | 6.25:1 | 4.5:1 | Pass |
| Active navigation / primary button text | `#ffffff` | `#0f6b63` | Normal | 6.36:1 | 4.5:1 | Pass |
| Accent link on white | `#0f6b63` | `#ffffff` | Normal | 6.36:1 | 4.5:1 | Pass |
| Body text on surface | `#101928` | `#f1f5f4` | Normal | 16.03:1 | 4.5:1 | Pass |
| Body text on soft surface | `#101928` | `#dce9e7` | Normal | 14.14:1 | 4.5:1 | Pass |
| Accent text on soft surface (after fix) | `#0f6b63` | `#dce9e7` | Normal | 5.10:1 | 4.5:1 | Pass |
| Accent text on accent-soft | `#0f6b63` | `#ccfbf1` | Normal | 5.64:1 | 4.5:1 | Pass |
| Hover accent on soft surface | `#115e59` | `#dce9e7` | Normal | 6.09:1 | 4.5:1 | Pass |
| Large headings | `#101928` | `#ffffff` | Large | 17.62:1 | 3.0:1 | Pass |

## Defect found and correction

- Initial accent colour `#0f766e` against soft surface `#dce9e7` measured **4.39:1**, below the 4.5:1 AA requirement for normal text.
- Updated the shared `--accent` token in `CSS/styles.css` to `#0f6b63`. The same pair now measures **5.10:1**, meeting AA.
- The updated accent also gives **6.36:1** against white and **5.64:1** against the accent-soft background.

## Scope and limitations

- These measurements cover the main text/background combinations identified in the stylesheet. Recheck any additional combinations or states that appear in the rendered pages, especially form controls and focus indicators.
- Borders and focus outlines are non-text contrast considerations; this table records text contrast only.
- Keep a screenshot of the contrast checker or calculation evidence if the instructor requires screenshots. The ratios above were calculated from CSS colour values, not visually estimated.
