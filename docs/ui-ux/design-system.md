# Mediku Design System — Foundation

**Status:** Draft foundation. Values below are provisional until visual QA and accessibility checks.

## 1. Design principles

- Playful, not childish.
- Friendly, not cluttered.
- Soft surfaces, strong text contrast.
- Consistent spacing and component behavior.
- Mobile-first and touch-friendly.
- Clinical content readability takes priority over decoration.

## 2. Provisional color tokens

Use semantic tokens in implementation rather than scattering raw hex values.

| Token | Provisional value | Intended use |
|---|---|---|
| `brand.primary` | `#7656D8` | Primary brand action and emphasis |
| `brand.primary-soft` | `#F0EBFF` | Soft brand surface |
| `accent.mint` | `#65CDB2` | Progress and positive feedback |
| `accent.blue` | `#8CBCEB` | Informational accents |
| `accent.coral` | `#FF9B8F` | Warm secondary emphasis |
| `surface.base` | `#FFFCF8` | Main warm background |
| `surface.card` | `#FFFFFF` | Card surface |
| `text.primary` | `#29253A` | Main text |
| `text.secondary` | `#777386` | Supporting text |
| `border.subtle` | `#EAE6F1` | Dividers and outlines |
| `state.success` | `#258A70` | Success state |
| `state.warning` | `#B97824` | Warning state |
| `state.error` | `#C34D5B` | Error state |

These values are visual starting points, not guaranteed accessible combinations. Check actual foreground/background pairings before shipping.

## 3. Typography

Provisional direction:
- Friendly sans-serif for headings and prominent labels.
- Highly legible sans-serif for body text, questions, explanations, and clinical content.
- Use a consistent type scale rather than arbitrary per-screen sizes.

Suggested semantic roles:
- Display: campaign and major result headings.
- Heading 1–3: page and section hierarchy.
- Body: clinical explanations and learning content.
- Label: metadata, status, and controls.
- Caption: secondary metadata only; never use for essential clinical information.

Do not use decorative fonts for medical content.

## 4. Spacing and shape

Use a consistent 4px base spacing scale. Suggested spacing tokens: 4, 8, 12, 16, 20, 24, 32, 40, 48px.

Suggested radii:
- Small controls: 10–12px.
- Standard cards: 16–20px.
- Large feature surfaces: 24px.
- Pills: fully rounded where semantically appropriate.

Shadows should be subtle and used to establish hierarchy, not as decoration on every element.

## 5. Component families

Build and document reusable components for:
- Buttons: primary, secondary, tertiary, destructive, disabled, loading.
- Navigation: mobile bottom navigation, desktop sidebar, active states.
- Cards: mission, campaign, learning activity, progress, achievement.
- Progress: bar, ring, level indicator, mastery indicator.
- Feedback: success, hint, explanation, warning, error.
- Inputs: text, search, choice, multi-select, answer submission.
- Overlays: modal, bottom sheet, tooltip, confirmation.
- Learning: case evidence, timeline, clinical finding, answer rationale.
- Game layer: XP reward, level-up, badge, collectible clue.

Do not build all components speculatively. Create components when a real screen/task needs them, then generalize repeated patterns.

## 6. Interaction states

Every interactive component must define relevant states:
- Default.
- Hover (where applicable).
- Focus-visible.
- Pressed/active.
- Selected.
- Disabled.
- Loading.
- Error.
- Success.

For learning activities, also consider:
- Answer submitted.
- Correct / incorrect feedback.
- Explanation expanded.
- Retry available.
- Activity resumed.

## 7. Accessibility baseline

- Maintain readable contrast for text and controls.
- Do not communicate status through color alone.
- Provide keyboard access and visible focus for interactive elements.
- Respect reduced-motion settings.
- Use semantic headings and controls.
- Give meaningful accessible names to icon-only controls.
- Keep touch targets comfortably large (aim for at least 44×44 CSS px where practical).
- Support zoom and text resizing without clipping.
- Avoid essential content in images without equivalent text.

## 8. Responsive breakpoints

Do not bind layout decisions to device brand names. Use content-driven breakpoints.

Provisional ranges:
- Small mobile: 320–374px.
- Standard mobile: 375–767px.
- Tablet: 768–1023px.
- Desktop: 1024px and above.

Validate real content at 320px and at common desktop widths. These ranges may be adjusted to the chosen framework and component behavior.

## 9. Dark mode

Dark mode is not a confirmed MVP requirement. Do not implement a separate dark visual system until it is explicitly prioritized. Clinical reading comfort and consistency take precedence.
