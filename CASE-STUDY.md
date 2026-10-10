# Case study: when a plausible plan does not fit the narration

## The problem

An AI-generated visual plan can look reasonable in text but fail when anchored to actual spoken audio. A detailed picture needs enough time for a viewer to understand it. Moving to the next image too early undermines the explanation.

## An observed incident

On 10 October 2026, Episode 011 had completed research, script and factual review, storyboard, and narration. Visual planning stopped at its second scene. Both saved planning attempts allocated approximately 5.3 seconds to a detailed picture while declaring that it needed a 7-second reading time.

The controller rejected both plans and preserved the completed upstream work. Packaging and delivery stayed pending. No extra provider request was made during the diagnostic review.

## What the incident demonstrates

- Validation uses measured narration timing, rather than accepting a plausible written plan.
- A bounded repair can still fail; exhausting that allowance produces a visible stop.
- A stage failure does not erase completed research or narration.
- A completed model response and a valid production checkpoint are different outcomes.

## Current improvement direction

Investigate how planning can use measured timing more effectively and whether a safe local consolidation can resolve the saved plan. This is proposed work, not a completed fix. The viewer-facing pacing constraint should remain intact.

## Verification limits

The local offline suite passed 702 Python tests and 24 renderer tests during this review. Passing tests does not resolve this saved production incident, guarantee historical accuracy, or measure whether viewers enjoy a video. This case study intentionally summarizes behavior without publishing the recovery implementation or proprietary prompts.
