# Postura — Customer Discovery

Customer interviews and prototype feedback conducted during development of **Postura**, a UCSD ECE 140B team project.

## Purpose

We investigated how students and desk-heavy professionals experience long sitting sessions, what prompts them to notice their posture, and whether a low-effort reminder would fit their routines.

Our starting hypothesis was that people often lose posture awareness while concentrating. We explored whether a chair-mounted device with quiet feedback could help them notice changes without requiring a wearable or constant self-monitoring.

## Interview Approach

We used semi-structured interviews covering daily activities, sitting habits, discomfort, existing workarounds, and preferred reminders. Later conversations included a product demonstration and questions about purchase interest and improvements.

The source notes contain **seven numbered interviews and four later feedback entries**. One later entry revisits the hospital worker, and another does not identify the participant. These entries are not treated as 11 unique participants. An earlier five-interview summary in the draft represents an interim synthesis.

Names and identifying details have been omitted from this public summary. Participant labels below are used only to organize the notes; responses are paraphrased.

### Participant Overview

| Entry | Background | Main observation |
|---|---|---|
| P1 | University student and library worker | Concentrating on posture can itself be distracting; preferred vibration in a quiet setting. |
| P2 | Computer science student | Reported slouching but little immediate concern; preferred a desktop notification. |
| P3 | Computer engineering student | Often noticed posture when sore or ready to stretch; preferred a small vibration, potentially on the wrist. |
| P4 | Computer science student | Associated posture with confidence; preferred vibration and already took regular movement breaks. |
| P5 | Remote fund accountant | Deadlines reduced awareness; wanted a passive chair-based solution rather than something to put on daily. |
| P6 | Nursing student | Used a footrest and noticed back discomfort; preferred an audible reminder. |
| P7 | Hospital monitor technician and unit secretary | Work took priority over posture; preferred gentle vibration that would not compete with hospital alarms. |
| P8 | University student; later demo feedback | Valued convenience, the pillow form factor, and break reminders. |
| P9 | Computer science student; later demo feedback | Liked buzzing feedback and suggested musicians as another possible audience. |
| Unlabeled entry | Background not recorded | Found a previous lumbar pillow inconvenient and expressed interest in vibration feedback. |

The later conversation with P7 added feedback about reaching for desk items, false alerts, and an on/off control.

## Key Findings

### 1. Concentration reduced posture awareness

Participants described losing awareness while studying, completing assignments, gaming, meeting deadlines, or handling hospital responsibilities. Fatigue and studying alone also appeared in the notes.

**Design implication:** Monitoring should require little ongoing attention and fit into an existing sitting routine.

### 2. Discomfort often prompted awareness, but motivation varied

Several participants noticed their position after soreness, fatigue, or discomfort. Others noticed proximity to a screen, shoulder position, or a pause in concentration. Some reported little pain or little urgency to change their habits.

Numeric estimates of time spent in self-described poor posture ranged from **40% to nearly 100%** among entries providing a clear percentage. These were personal estimates, not sensor measurements; not every participant supplied a percentage.

**Design implication:** Explore reminders that support awareness before users would normally notice, without assuming every user is motivated by pain or that the device prevents it.

### 3. Convenience mattered

Existing approaches included pillows, ergonomic chairs, footrests, chair adjustments, stretching, and other personal measures. Several participants used no dedicated posture product.

The remote professional explicitly favored a chair-mounted device because wearing something every day could be inconvenient. Later feedback supported the pillow concept, but another participant described a previous lumbar pillow as inconvenient. One student suggested wrist vibration.

**Design implication:** A chair-mounted approach was promising, but mounting comfort and repeated use still needed testing. The interviews did not establish a universal rejection of wearables.

### 4. Feedback preferences differed

Vibration appealed to several participants, particularly in libraries and hospital settings. However, one student preferred a desktop notification and another preferred sound. Participants also differed on whether correcting posture improved focus or interrupted it.

**Design implication:** Use quiet haptic feedback as the prototype's main reminder while evaluating alert timing, intensity, and user control.

### 5. Normal movement should not cause unnecessary alerts

In follow-up feedback, the hospital worker raised concern about reminders while reaching for nearby items and suggested an on/off feature. Interest in using the product was conditional on additional testing.

**Design implication:** Distinguish temporary movement from sustained posture changes and explore a pause control.

## Prototype Feedback and Design Decisions

| Feedback | Response or next step |
|---|---|
| Users lose awareness during focused tasks. | Develop automatic sensing with an upright calibration baseline. |
| Several participants favored quiet reminders. | Use vibration feedback in the prototype. |
| A professional wanted a device that did not need to be worn daily. | Pursue a chair-mounted form factor and test comfort and convenience. |
| Demo participants liked break reminders. | Include movement-break reminders and suggested stretches in the web experience. |
| A student wanted a distinct reminder for breaks. | Consider separate vibration patterns for posture and break alerts. |
| A professional worried about alerts during reaching. | Prioritize false-alert testing and a future pause/on-off feature. |
| One participant suggested musicians. | Treat musicians as a possible future interview group, not a validated market. |

## Early Pricing Signals

Recorded hypothetical spending responses included **$20**, **$20–$30**, **$30–$35**, and **$50**. The remote professional discussed budget constraints without naming a price.

These responses suggest affordability is worth testing. They do **not** establish a validated selling price: several questions asked what someone would pay for “perfect posture,” which promises more than this prototype demonstrates. No purchases or preorders are documented in these notes.

## What We Learned—and What Remains Open

The interviews supported further exploration of automatic posture reminders, quiet feedback, and convenient mounting. They also challenged the assumption that everyone who reports slouching wants a product or would accept frequent interruptions.

This was a small, exploratory sample. Questions sometimes suggested answer choices, referenced earlier participants' preferences, or assumed that posture correction would improve health or productivity. Those prompts may have influenced responses.

The draft's greater-than-90% classification accuracy target was a **proposed goal**, not an achieved result. Interview feedback does not establish detection accuracy, pain reduction, sustained use, or purchase conversion.

## Next Validation Steps

- Observe whether users continue using the prototype across multiple study or work sessions.
- Record false alerts during reaching, shifting, and leaving the chair.
- Compare alert timing and intensity, including an option to pause feedback.
- Test mounting comfort across different chairs and users.
- Evaluate classification against independently labeled observations.
- Test purchase interest using the actual prototype, its limitations, and a specific price.

The central opportunity is a reminder that fits into users' routines with little effort. Whether Postura delivers that experience reliably requires continued technical and usability testing.

---

**Team:** Aden Tan, Alex Wei, Colin Hua, and Richard Kim  
**Course:** UCSD ECE 140B  
**Source:** Team interview notes and prototype feedback collected during project development.
