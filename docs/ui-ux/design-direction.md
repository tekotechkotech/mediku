# UI/UX Design Direction

**Status:** Direction agreed; detailed design tokens and screens remain to be validated.

## 1. Design intent

Mediku should feel like a friendly, engaging learning companion with the depth of a clinical adventure game.

**Keywords:** playful, friendly, modern, polished, approachable, clear, encouraging.

The product should be enjoyable without becoming childish, noisy, or medically unserious.

## 2. Audience consideration

The initial pilot learner is female, and the agreed preference is playful learning. This is a product context, not a reason to stereotype the visual language.

Do not assume femininity means pink, cute characters, or excessive decoration. Use a balanced, inclusive palette and polished illustrations that can appeal broadly to medical students.

## 3. Visual inspiration

Borrow principles, not exact UI, from:
- Duolingo: approachable learning loops, clear progress, encouraging feedback.
- Investigation/adventure games: clues, case progression, discovery, meaningful unlocks.
- Modern medical education products: readable clinical content, trust, and visual clarity.

Avoid copying proprietary visual assets, characters, or layouts.

## 4. Visual direction

### Palette direction

Explore a soft, optimistic palette:
- Lavender / purple as a potential brand anchor.
- Soft blue for calm informational surfaces.
- Mint / teal for progress and positive actions.
- Coral for selected emphasis and warmth.
- Warm cream / off-white for comfortable reading.
- Dark neutral text for legibility.

This is a direction, not a locked palette. Exact color values must be finalized in the design system and checked for contrast.

### Typography

- Friendly, rounded sans-serif may be used for headings and prominent UI.
- Body and clinical content must prioritize legibility over stylistic personality.
- Keep a clear hierarchy and avoid overly small text.

### Components and shape language

- Rounded cards and clear grouped surfaces.
- Pill-shaped controls where they improve clarity.
- Progress rings/bars and compact achievement indicators.
- Generous spacing and touch-friendly controls.
- Consistent icon family and restrained use of decorative elements.

### Illustration and character

- Simple, expressive medical illustrations may make learning approachable.
- A mascot/companion is a possible brand element, not a mandatory element on every screen.
- Illustrations must not replace clinically accurate diagrams where precision matters.
- Medical tools, anatomy, and procedures must be checked for accuracy before being used as instructional visuals.

### Motion and feedback

- Use lightweight micro-interactions for selection, progress, success, and transitions.
- Motion must be quick, purposeful, and respectful of reduced-motion preferences.
- Do not use animation that delays a learner or obscures important clinical information.

## 5. Mobile-first responsive behavior

Mobile is the primary design target:
- Start wireframes at narrow mobile widths.
- Use bottom navigation for the four primary areas.
- Keep primary actions within comfortable thumb reach.
- Prefer one-column layouts and progressive disclosure.
- Avoid dense tables and multi-panel interfaces on small screens.
- Make touch targets comfortably sized.
- Keep learning flows focused and easy to resume.

Desktop is an expanded responsive experience:
- A sidebar may replace bottom navigation.
- Use wider layouts or two-column arrangements when they improve case reading and evidence comparison.
- Do not simply stretch mobile cards across the full viewport.
- Preserve the same information architecture and design tokens.

## 6. Primary navigation

Four areas only:
1. Home — activity center, current campaign, recommended mission, continue learning.
2. Campaign — rotation journeys and progression.
3. Learn — cases, simulations, challenges, and learning resources.
4. Progress — topic mastery, learning history, and knowledge gaps.

Profile and settings are accessible from the account area, not a fifth primary destination.

AI tutor should appear contextually inside an activity rather than automatically receiving a primary navigation slot.

## 7. Home screen intent

Home should answer:
- What campaign am I currently in?
- What is the most useful next activity?
- Where did I leave off?
- Am I making progress?

Suggested content:
- Current campaign summary.
- One recommended mission with a clear start/continue action.
- Continue learning card if an activity is in progress.
- Compact progress snapshot.
- Recent activity only when useful.

Avoid presenting a long task list or every available module at once.

## 8. Experience principles

- Maximum 2–3 interactions from Home to starting a learning activity.
- Typical learning sessions: 5–20 minutes.
- Save activity progress automatically when feasible.
- Provide useful explanations after mistakes; do not punish mistakes.
- Separate campaign completion, academic task completion, exam readiness, and topic mastery.
- Keep streaks encouraging and non-punitive.
- Do not create guilt-inducing return states or notification pressure.

## 9. Design maturity

The current direction is approved as a starting point, not a finished design system. Exact tokens, typography, components, screen specifications, and interaction states require design review and validation.
