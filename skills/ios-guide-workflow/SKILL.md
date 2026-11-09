---
name: ios-guide-workflow
description: "Build, refine, and verify interactive guides, walkthroughs, coach marks, and feature tours inside native iOS apps. Use for guide creation or feedback about steps, targeting, interaction, return behavior, readability, or progress. Clarify ambiguous guide requests. Screen recording, video production, and navigation unrelated to a guide are outside this workflow."
---

# iOS Guide Workflow

Create an app-specific guide using the target project's real screens, design system, navigation, and data rules. Reuse existing platform features, guide components, and tests before adding infrastructure.

## Start with project discovery

Read the applicable project instructions, relevant product decisions, existing guide implementation, design system, navigation owners, data boundaries, and test entry points. Discover these in the target project; this skill has no required product-specific paths, identifiers, assets, dependencies, or palette.

Identify the requested outcome and whether the work creates a guide, corrects an existing step, or checks a reported failure. Preserve unrelated work. Read existing answers and accepted decisions before asking questions. Use the current request to update their scope, and resolve a material conflict rather than silently choosing between incompatible decisions.

If a request such as "make a guide video" still leaves the deliverable unclear after project discovery, ask one question before implementation. For example, "Do you mean a step-by-step guide that users follow inside your iOS app?" Once the in-app guide is clear, use the app's actual screens and controls and ask only for the missing decisions below. Screen recording, video editing, and promotional video production are outside this workflow.

Briefly summarize the established facts and any critical gaps relevant to this task. Discover theme values, component paths, navigation structure, build schemes, and test entry points directly when the project provides them.

## Ask only for missing key decisions

For a new project or guide, check the relevant areas below against the current request and project records:

- Teaching goal: intended audience, what to explain or practice, and the outcome that counts as success.
- Entry and completion: trigger, eligibility, automatic frequency, manual replay, and whether progress tracks the current run, durable completion, or a particular revision.
- Interaction: informational, exploratory, or action-gated steps; selection and confirmation; automatic advancement, back, skip, and read-only controls.
- Data: existing user data, practice data, or temporary examples; behavior when suitable data is missing; retention or cleanup after completion, skip, interruption, and replay.
- Visual exceptions: any requested highlight scope, connector style, or endpoint rules beyond the app's existing design system.
- Verification and delivery: priority devices and supported configurations, relevant acceptance checks, and evidence such as test results or screenshots.

Ask only when an unresolved answer materially affects the teaching goal, behavior, data, visual direction, or verification scope. Combine related gaps into a short batch of focused questions; offer clear choices when useful and identify any proposed default. A question list is not a requirement to ask every question or repeat a documented answer.

For a focused correction, revisit only decisions changed or left unresolved by that feedback. Resolve routine implementation details from the project and proceed when the needed decisions are clear, without adding a separate approval round for an already-authorized task.

If a required decision is unanswered, keep it open and wait before dependent implementation or data changes. Continue independent inspection or reproduction. Silence is not confirmation of a proposed policy.

## Keep answers in the target project

Save answers and accepted decisions in the target project's existing specification, decision record, or correction log. If no suitable record exists, use a small project-local document consistent with its conventions. Do not prescribe a universal filename or require a separate storage service.

For each relevant decision, retain the choice, its guide or step scope, rationale when known, and remaining questions. Distinguish user-confirmed decisions, established project behavior, and proposed defaults. Keep later clarifications and superseded decisions traceable.

Read this record before the next correction and ask only about material changes or gaps. Keep all project answers, identifiers, palettes, examples, and implementation context in that project; never copy them back into this skill or its bundled resources.

Use a small step map when the flow spans multiple screens. For each affected step, capture its purpose, highlight region, pointer target if any, allowed controls, forward condition, return destination, and data effects. Internal loading or dismissal transitions need not become visible teaching steps.

Follow an explicit product decision about permissions or progression. A descriptive step can be read-only; an exploratory guide can leave controls available. Do not impose one locking, skip, or return policy on every app.

## Match the guide to its teaching goal

For an action-focused introduction, put necessary concepts beside the action they explain. Remove optional chart interpretation or variant exploration from that guide when it does not serve the goal; preserve the app's features and guides whose purpose is explanation. Use the requested native preview without requiring unrelated exploration or external sharing. Prefill incidental setup when appropriate, while keeping the action being taught real.

For independent section guides, give each its own entry, progress, and completion according to the product's policy.

Decide what question the user should be able to answer before choosing sample data for a chart guide. Choose inputs that make the relevant comparison visible in the app's actual output. A steady metric can help answer the question when the guide compares it with another measure.

In the prompt, name the action, point to the value to read, and explain what conclusion the displayed results support. Use matching filters and corresponding time windows when comparing values across charts. Explain how filters change which records are included. Identify the population, measure, time unit, and each metric's denominator where applicable.

When a lesson uses multiple measures, explain what each measures and what a rise or fall means before interpreting them together. Use comparable examples to show what their combined changes reveal. Include measures moving in the same direction when that case helps answer the teaching question.

When explaining phases on a timeline, follow one concrete example across all the phases. Point out the event that marks the transition, show where it appears on the chart, and explain what to look for in each phase.

If a wide chart is hard to read on a phone, show the segment for the current phase or comparison at a readable scale. Keep the labels, units, and legend that connect each segment to the rest of the chart.

When displaying progress, derive position and total from the actual visible step map. Define how the invitation is counted, count visible substeps consistently, exclude hidden transitions, and update progress on back or a revised flow. Do not combine several visible prompts into one reported step to disguise length. Keep progress readable, localized, and secondary to the current task using the app's design system.

Localize guide copy, progress formats, and sample names through the target app's supported resources. Keep practice-specific defaults local to the run without changing the user's language or other preferences. For examples spanning dates, use one stable run date and the app's calendar/time-zone rules.

## Use the target app's visual language

Resolve background, surface, primary and secondary text, accent, border, focus, and enabled/disabled colors through the target app's existing theme or semantic colors. Support the themes that app already supports. A color that works against one surface is not evidence it works against another.

Reuse native controls and existing components. Keep brand colors, typography, spacing, and motion decisions in the target project. If the required design direction is missing, ask for that decision rather than importing another product's look.

Treat these as separate concepts:

- The region highlighted to explain a group or screen.
- The semantic point a connector should identify.
- The controls the current step permits the user to operate.

A wider highlight does not enable its descendants. An endpoint should identify the teaching target while avoiding meaningful content where possible; a short or direct line must not change what the step points to. Use the existing connector style, and omit a connector when it adds no useful association.

When explaining a whole component, highlight its outer rendered bounds, including its relevant heading, icons, body, and empty or unavailable states. Use the same outer target across consecutive steps that explain that component. Narrow the highlight when a step teaches a specific control or subregion. Measure expanded components in their current state. Keep the actual control and tooltip avoidance region separate when only part of that content is interactive. If the group exceeds the viewport, preserve normal scrolling and the reachable control rather than shrinking or duplicating the content.

Attach each visible connector to the rendered tooltip and highlight outlines. Choose the highlight endpoint along the edge that best identifies the teaching target and leaves text and controls clear. If the design uses an endpoint marker, center it on that outline. A rounded rectangle's bounding-box corner may sit outside the visible shape.

Route the line through the gap between the outlines. If they overlap or leave too little space for a clear route, omit the line and marker together. Recompute after expansion, scrolling, keyboard changes, and return transitions. Verify both endpoints and clearance with long labels and larger text. Require horizontal and vertical segments only if the app's style calls for them.

Keep buttons recognizable and their disabled state clear. Retain native focus and accessibility semantics, adequate hit areas, and contrast against the actual rendered surface. Decorative overlays should not become duplicate accessibility content.

## Measure the real presentation

Measure the intended control, including relevant native accessories or expanded content, before adjusting visual padding. Use the target's actual window, scene, presentation hierarchy, transforms, and visible bounds.

Account for safe areas, bars, keyboards, sheets, scrolling, rotation, and Dynamic Type when they affect the target. An internally rotated view does not prove the device interface was tested in landscape.

Include rendered text extents, borders, and surrounding padding when checking visibility. Increasing highlight padding alone cannot fix clipping at a viewport edge.

Choose positioning from the space required by the target and explanation together. Centering, top alignment, side placement, and independent scrolling are context-dependent choices. Do not reserve empty action rows or derive a zero-height explanation from a full-screen highlight.

Wait for observable data readiness, completed presentation, or stable visible geometry before enabling the relevant action. Avoid a fixed delay that merely guesses readiness. If the target is unavailable, use the project's loading, scrolling, retry, or interruption behavior instead of guessing a coordinate.

When a step scrolls or navigates to a target, wait for the movement to finish and measure the target at its settled position before showing the highlight and prompt. Use the app's motion style for the reveal. With Reduce Motion enabled, wait for the same placement, then show the highlight and prompt directly without a reveal animation. Verify this order when moving forward and back in both motion settings.

When an interaction leaves the active step and rendered highlight bounds unchanged, keep the highlight, prompt, and any connector in place. Update only the prompt content and action state. Keep the current scroll position and skip the entrance transition. Use the normal placement checks when the step changes or the target needs to move.

Check custom gesture and touch overlays as well as outer disabled flags. A native control's automation metadata may describe a different interaction layer from the one receiving real input.

Match the hit region to the full visible surface of controls intended to be fully tappable. Check nearby decorative layers when touches fail, since visible clipping and hit boundaries can differ. Keep decorative layers from intercepting touches and preserve neighboring controls' intended behavior.

## Handle keyboard states explicitly

For text-entry steps, check the keyboard opening, visible during input, and closing. After actual keyboard and scroll layout changes, measure the focused field including its decoration and visible value, tooltip, and required confirmation, back, and exit controls. Account for safe areas and scroll insets without shrinking accessibility text to make them fit. Use observable focus, keyboard-frame, and presentation events instead of fixed delays.

For search or editing that reflows content, recheck the field after focus, text changes, and actual keyboard-frame changes. Initial visibility or a hit-test flag cannot prove the field remains inside the usable viewport while typing. Preserve the app's intended submit and interactive keyboard-dismissal behavior.

If scrolling to a nested identifier aligns the enclosing row, locate the actual focused native control and its owning scroll view, convert their coordinates, and clamp adjusted offsets to the valid scroll range. Recheck the result after scrolling; a requested offset is not evidence that the control is visible.

Coordinate focus changes, step changes, save/cancel, and dismissal through the existing editing and presentation owners. Release temporary control references when editing or the screen ends. Reproduce keyboard-related save or dismissal failures through the reported entry path and collect diagnostics before assigning a cause; a longer timeout is not a fix.

## Advance and return through actual events

Separate selection, confirmation, submission, navigation, and animation completion. When a step requires practice, a preselected value alone is not evidence that the user performed the action. Preserve room to adjust a choice when the product requires confirmation.

Accept only the current step's relevant event and valid data identity. Repeated taps, delayed responses, failed saves, or events from an ended run must not advance a later step or repeat a write.

For gesture practice, define the permitted action and direction, and count successful state changes rather than attempted gestures or duplicate callbacks. Separate prefilled history from actions performed in this step, and verify the resulting totals after back, retry, or replay against the app's data semantics.

Use the actual navigation or presentation owner to open, close, and return between screens. Sequence dependent transitions through their completion events. Changing only the tooltip text does not restore the previous screen.

Scope interaction locks to the controls they govern. Inspect inherited enabled state and accessibility identifiers when a guide enters a presented screen. Keep its required actions available and verify the target again after actual dismissal.

Coordinate root-container changes with child pop or dismissal transitions so they do not race. Invalidate obsolete navigation work and rebuild guide anchors only after the destination hierarchy is ready; a changed root selection alone does not prove that its native content is visible.

When back is supported:

- Define which visible step it returns to and whether the previous action is editable, read-only, or safe to repeat.
- Preserve valid selections; reuse the intended records rather than creating another copy.
- Restore prior state only within the current run's authorized ownership and live data. Never recreate deleted or unrelated records from a stale snapshot.
- Prevent duplicate submissions, accumulated side effects, and late callbacks from a cancelled transition.
- Keep the product's exit behavior available during intermediate transitions.

Use real previews and product feedback. A read-only teaching step must not silently export, request a permission, publish, purchase, or change account preferences. Respect authorization for any external effect.

## Define data and completion separately

Establish the retention policy before writing or deleting guide-related data. Use the project's existing ownership and provenance mechanisms to identify records created for the current practice run. Do not infer deletion scope from dates, record counts, or an otherwise empty account.

When practice data must be removed, extend cleanup and supported backup exclusion to each new practice record type and relationship before claiming complete cleanup. Preserve real records connected to practice data; identify ownership rather than deleting an entire connected group. Explain aggregate screens using their actual data instead of assuming an otherwise empty account.

Check normal completion, skip, interruption, retry, relaunch, account changes, replay, and backup/restore where applicable. If practice data must be cleaned up, preserve recoverable cleanup intent when persistence fails and prevent excluded data from reappearing through supported backup paths. If the guide uses real user data, preserve it according to the product contract.

If a run removes a record that owns a visible destination, coordinate dismissal with that destination's actual owner so an obsolete editor cannot write it back.

When the product displays that a guide has ever been completed, distinguish that fact from the latest run's status. Define the completion event, replay behavior, compatibility, restore/merge rules, account boundary, and any version-reset policy. Preserve known history; do not invent missing history. A status indicator should follow the product's intended editability and semantics.

Define automatic invitation eligibility separately from presentation, interruption, and successful completion. If the product consumes eligibility only on explicit completion or skip, leaving or terminating the app must not imply either decision; apply its agreed restart or resume policy. Preserve known resolution through replay and restore within its account and revision scope, while keeping a skip distinct from completion. A legacy record that proves only prior presentation cannot prove a user decision. Where remote state exists, handle delayed responses and offline deferral without unbounded retries or competing presentations.

Keep temporary teaching examples clearly defined and isolated from normal storage and preferences. Introduce them only when the task or product decision calls for them, reuse real components, and verify their removal or retention explicitly.

For sample analytics, supply reproducible isolated inputs to the app's real calculations and controls. Use transient inputs when persistence is unnecessary, and keep sample and user results separate in caches. Check that results match the current data source and filters before presenting an interpretation.

When a sample analytics guide completes, is skipped, or is interrupted, restore the user's prior view settings before loading real results. Use the same restored settings for the visible controls and the request or calculation. Ignore late sample results after exit. Verify that the displayed results match the real data source and restored controls.

## Verify the affected behavior

Choose checks proportional to the change and use the target project's existing tools:

- State and data changes: focused tests for valid and invalid events, return/replay effects, identity, persistence, and failure paths. Leave a minimal runnable behavioral check for new non-trivial logic.
- UI changes: operate the real affected flow, including its forward path and relevant back, skip, cancel, and re-entry paths. A tooltip existing is not enough to prove the target can be read or operated.
- After an entry or its destination is redesigned, start from the current control and exercise each affected guide step. Check that the prompt names the current control and action, the highlight covers the rendered target, and the prompt leaves the required controls visible and usable at supported text sizes. When the step requires opening a screen, check that the prompt and progression reflect its actual presentation, including after going back and reopening it.
- For a shortcut that should reveal a guide entry, use the actual shortcut and verify that the guide button comes into view after the jump settles. Tap it from the resulting position without scrolling further, and confirm that it opens the intended guide. If the shortcut can expand the destination, test with the destination both collapsed and expanded.
- Updates within a step: compare the highlight and prompt positions before and after the interaction, and verify the new content and action state. Then advance and check that the new step is presented at its own target.
- Text entry: operate keyboard opening, typing, closing, step changes, save/cancel, and relevant exit or re-entry paths on the affected small-screen and text-size configurations. Check the visible value and resulting state as well as geometry; keyboard-hidden screenshots cannot validate editing.
- Layout changes: inspect affected small and regular layouts and accessibility text sizes. Include supported themes, languages, right-to-left layouts, keyboards, or orientations when the change or claim depends on them. Verify actual frames and rendered results.
- SDK or concurrency failures: exercise the real callback path under relevant build/runtime conditions. Inspect callback isolation and captured values; do not assume every callback uses the same queue. A fake or disabled integration cannot validate a path it bypasses.

Discover the current build scheme, focused test targets, and available destinations rather than copying another project's commands. Use isolated test data. Investigate automation hierarchy and actual input results before treating a missing identifier or hit-test flag as a product failure.

For a hit-area regression, exercise the affected screen state and tap the visible control at multiple coordinates, including inner edges, icons, and whitespace. Verify the expected transition independently at each point and check neighboring controls after changing their hit boundaries. Use fixtures that render the affected state and include the regression in an existing verification job that runs it. Record execution results separately from build and test configuration checks.

An accessibility group's frame can omit rendered content such as decorative icons. Compare the highlight with every relevant edge of the rendered component in each affected step. For custom touch overlays, verify actual input, the changed value, and the expected progression state alongside geometry and screenshots; a hit-test flag alone does not settle whether the control works. When applying a correction across guides, inspect each affected step and retain already-correct layouts rather than enlarging every highlight or copying one padding value everywhere.

Keep build failures, runtime failures, automation failures, resource exhaustion, and unavailable evidence distinct. Repeat a check when a fix or unresolved concern warrants it; avoid rerunning unrelated suites without a reason.

When memory or simulator capacity is constrained, run native builds and tests sequentially, using one compatible destination at a time. Reuse available task resources before starting more. Release task-owned idle resources and keep unrelated sessions, shared build caches, and delivered artifacts intact.

Identify the tested source/build and the device, OS, theme, language, text size, and orientation relevant to the claim. A commit does not fully identify an uncommitted workspace. Preserve useful results and selected screenshots in the project's established QA location; temporary logs need a durable summary when long-term evidence matters.

When unrelated workspace edits could affect a scoped delivery, verify the intended patch against its stated clean base in an isolated source snapshot. Include required build resources from that base, and distinguish an incomplete snapshot from a real dependency on excluded changes. A wider workspace pass does not prove that the delivered patch works independently.

When reviewing an existing recording of guide behavior, associate it with the build it captured. Later validation establishes evidence for the build tested in that run.

Report only the tested scope. Count distinct scenarios separately from repeat executions, including reruns on an isolated source snapshot. Simulator tests, an archive, a processed upload, device execution, VoiceOver operation, and human acceptance are separate evidence. Do not combine earlier and later runs into a fictional all-passing final build. Being operable also does not mean all teaching content fits on screen at once.

## Record feedback and deliver

When maintaining correction history, use the target project's existing record and keep one entry per independent issue. Capture:

- Feedback verbatim or explicitly marked as a summary, with context and source/build when known.
- Expected behavior and rationale, confirmed cause or remaining uncertainty, and the smallest fix.
- Reproduction and evidence, implementation/test status, and human acceptance separately.
- A possible reusable lesson with its conditions, and any earlier decision it supersedes.

Update an existing issue as work proceeds. Preserve superseded decisions as history; do not carry their old expectations into current checks. Mark unknowns instead of filling them with plausible details.

Conclude with the changed behavior, relevant verification and evidence, and the specific judgments or checks still pending. Keep project names, paths, identifiers, palettes, domain examples, and implementation details in the target project's records. Do not write them into this skill or its bundled resources.
