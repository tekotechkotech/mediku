# Information Architecture and User Flows

## 1. Primary navigation

Keep four primary destinations:

| Destination | Purpose | Typical contents |
|---|---|---|
| Home | Resume and discover the next useful activity | Active campaign, recommended mission, continue learning, compact progress |
| Campaign | Understand rotation journey and progression | THT-KL campaign, Anesthesiology preparation campaign, milestones |
| Learn | Enter learning experiences | Clinical Investigation, DOPS Simulator, Knowledge Challenge, Exam Arena |
| Progress | Understand learning outcomes | Topic mastery, strengths, knowledge gaps, history |

Profile/settings belong in the account area, not the primary navigation.

## 2. Core flows

### First-time learner
Onboarding → profile basics → current campaign → Home → recommended first activity.

Keep onboarding short. Do not ask for data that is not needed to begin learning.

### Returning learner
Home → Continue Learning or Recommended Mission → activity → feedback/result → progress update → next recommendation.

### Clinical Investigation
Mission intro → synthetic case brief → history → examination findings → choose/interpret investigations → differential diagnosis → most likely diagnosis → management decision → feedback and explanation → result.

Evidence can be revealed progressively. Wrong answers should produce useful explanations and allow recovery; they should not create punitive failure loops.

### DOPS Simulator
Skill overview → indication and safety context → preparation and equipment → ordered steps → technique/safety decisions → feedback → retry or completion summary.

Make it explicit that the simulation is not official DOPS and does not replace supervised practice.

### Knowledge Challenge
Select or receive a topic → answer a short question set → explanations → review weak concepts → schedule or recommend future review.

### Exam Arena
Choose assessment type → read case/instructions → simulated assessment → rubric-based feedback → improvement plan.

## 3. Home screen hierarchy

1. Greeting / learner context, kept compact.
2. Active campaign.
3. One recommended mission or Continue Learning card.
4. Compact learning progress.
5. Recent activity or next suggested action, only when useful.

Do not put every learning category, all campaign milestones, all achievements, and a long to-do list on Home.

## 4. Campaign model

A campaign represents a rotation learning journey, not administrative completion.

Initial campaign context:
- THT-KL: active.
- Anesthesiology: preparation.

Campaign progress should reflect learning activities and topic coverage, not imply official rotation sign-off or clinical competence certification.

## 5. Responsive navigation

Mobile:
- Bottom navigation with four destinations.
- One-column content.
- Primary action within comfortable thumb reach.

Desktop:
- Sidebar navigation may replace bottom navigation.
- Wider content container and optional two-column layouts for case details/evidence.
- Preserve information architecture and hierarchy.

## 6. Screen inventory

Initial screens to specify and design:
1. Onboarding / profile basics.
2. Home.
3. Campaign overview / selection.
4. Learn hub.
5. Clinical Investigation.
6. DOPS Simulator.
7. Knowledge Challenge.
8. Exam Arena.
9. Progress / knowledge gaps.
10. Profile and settings.

Screen designs should be developed one by one, starting with Home, then a representative Clinical Investigation flow.
