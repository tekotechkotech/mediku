# Mediku — Product Brief

**Status:** Initial product definition  
**Brand:** Mediku (working name; clearance not yet completed)  
**Previous project name:** Medical Quest

## 1. Product vision

Mediku is an RPG-inspired clinical learning platform that helps medical students transform clinical exposure into deeper understanding and stronger clinical reasoning.

**Core principle:** The hospital gives students clinical exposure. Mediku turns that exposure into deeper understanding and stronger clinical reasoning.

## 2. Problem

Clinical exposure is valuable but uneven. Students may not encounter every condition, procedure, diagnostic pattern, or emergency during a rotation. Real clinical environments also offer limited opportunities to repeat decisions safely, explore alternative cases, or make mistakes without consequences.

Mediku provides structured, repeatable, low-stakes practice that complements—not replaces—clinical training.

## 3. Positioning and boundaries

Mediku is:
- A gamified clinical learning platform.
- A practice environment for case reasoning, conceptual procedural skills, knowledge reinforcement, and simulated exams.
- A companion to clinical rotations.

Mediku is not:
- A koas administrative task manager or hospital checklist.
- A conventional file-first LMS.
- A patient-facing diagnostic tool.
- A substitute for supervised patient care, clinical placement, or official competency assessment.

Do not convert assignments such as video tasks, surgical reports, patient status reports, or official DOPS into mandatory app quests. The product must not create a second task manager.

## 4. Target users and initial context

Primary users are medical students in clinical rotations (koas). The initial pilot context discussed is:
- THT-KL: active campaign.
- Anesthesiology: preparation campaign.

Do not assume any further rotation sequence or official university curriculum. Rotation examples are illustrative and must be validated with educators and authoritative references.

## 5. Learning experiences

The conceptual learning domains are:
1. Clinical Case Investigation.
2. DOPS / Procedural Skills Simulator.
3. Long Case / Clinical Examination.
4. Knowledge Challenge.
5. Anatomy & Pathophysiology.
6. Diagnostic Interpretation.
7. Emergency & Decision Making.

These are content domains and experience types, not seven separate top-level navigation destinations.

### MVP priority: four experiences

**Clinical Investigation**
- Present a synthetic patient scenario and chief complaint.
- Reveal history and examination findings progressively.
- Let the learner select or interpret relevant investigations.
- Build a differential diagnosis.
- Choose a most likely diagnosis and management approach.
- Explain decisions and provide evidence-based feedback.

**DOPS Simulator**
- Practice indications, preparation, instruments, patient preparation, sequence, technique concepts, and safety.
- Provide step-by-step feedback and retry.
- Clearly state that simulation does not replace supervised practice or official DOPS.

**Knowledge Challenge**
- Adaptive quizzes, flashcards, spaced repetition, and error review.
- Focus on retrieval practice and knowledge retention.

**Exam Arena**
- Simulated long case, OSCE-style assessment, oral questioning, and rubric-based feedback.
- A virtual examiner may be used, with transparent scoring criteria.

Anatomy, pathophysiology, diagnostic interpretation, and emergency decision-making should be embedded in relevant cases, skills, challenges, and exams rather than exposed as separate primary modules.

## 6. Example content by rotation

Examples only; not official curriculum requirements.

**THT-KL**
- Cases: otitis, sinusitis, hearing loss.
- Skills: otoscopy and ENT examination.
- Diagnostics: audiometry and tympanometry.
- Anatomy: ear and upper airway.
- Emergency: epistaxis and airway obstruction.

**Anesthesiology**
- Cases: pre-anesthesia assessment.
- Skills: airway management concepts.
- Diagnostics: ECG and blood gas interpretation.
- Anatomy: airway anatomy.
- Emergency: resuscitation and anesthesia complications.

## 7. Learning and game mechanics

- XP is earned for meaningful learning actions and demonstrated understanding, not clicks.
- Level represents overall progression.
- Campaign progress represents progress through a rotation learning journey.
- Skill/topic mastery is tracked separately from campaign completion.
- Evidence collection can represent clues or findings gathered during investigations.
- Boss battles represent higher-difficulty simulated assessments.
- Streaks may encourage consistency but must not punish missed days.
- Avoid punitive hearts, guilt messaging, and loss mechanics that discourage safe mistakes.
- Completing an academic assignment does not imply mastery of its underlying topic.

## 8. AI Game Master

Potential responsibilities:
- Recommend a suitable next learning activity.
- Identify knowledge gaps from learner performance.
- Adapt difficulty and practice sequence.
- Generate practice questions from curated, approved sources.
- Explain answers and provide feedback.
- Act as a virtual examiner in simulated assessments.

Constraints:
- Do not fabricate references or clinical claims.
- Show uncertainty and source provenance.
- Do not present generated content as authoritative until reviewed under the content governance process.
- Keep AI assistance contextual to the learning activity.

## 9. MVP scope

Core:
- Authentication and learner profile.
- Campaign support for THT-KL and Anesthesiology.
- Home and learning navigation.
- Clinical Investigation experience.
- Quiz / Knowledge Challenge engine.
- Basic conceptual procedural skills simulation.
- XP and level foundations.
- Progress and topic mastery tracking.
- Basic knowledge-gap identification.
- Responsive mobile-first interface.

Next priorities, subject to validation:
- AI Game Master and contextual tutor.
- Exam Arena.
- Spaced repetition.
- Adaptive difficulty.
- Achievements and richer progression.

Future:
- Additional rotations.
- Advanced 3D anatomy.
- Rich interactive procedure simulation.
- Voice-based oral examination.
- Multiplayer/social learning.
- Educator content and analytics dashboard.

## 10. UX principles

- Powerful learning system, effortless experience.
- Complex system behind the scenes; simple interface in front.
- Mobile-first, with desktop as an expanded experience.
- Short sessions, typically 5–20 minutes.
- Maximum four primary navigation areas.
- Two to three interactions from Home to starting a learning activity.
- Progressive disclosure and automatic progress saving.
- Low cognitive load; avoid unnecessary tasks, notifications, and reward clutter.
- The app should be quiet and welcoming when a tired learner returns.

## 11. Safety and content governance

- Use curated, credible medical sources; record citations and review/update dates.
- Have qualified academic/clinical reviewers approve content before publication.
- Use synthetic or appropriately de-identified case data.
- Do not include patient-identifiable data without a valid legal and privacy basis.
- Distinguish fact, recommendation, simplification, and uncertainty.
- Simulation does not replace supervised clinical training or official assessment.

## 12. Success signals

Measure:
- Learning activity completion.
- Knowledge retention and improvement.
- Quality of clinical reasoning.
- Repeat practice and return learning.
- Campaign progression.
- Learner-reported cognitive load and usefulness.

Do not optimize only for session length, clicks, streaks, or gamification engagement.
