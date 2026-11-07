# iOS Guide Workflow

A skill for building, fixing, and testing step-by-step guides in SwiftUI and UIKit apps. Use the app's own screens, navigation, and theme to teach someone their first task or help them understand a feature.

## Demo

https://github.com/user-attachments/assets/2bcbe4b8-f139-4b79-b8a0-f79e9b40955e

## What it checks

| What can go wrong | How to check it |
| --- | --- |
| The keyboard covers the field or the next action. | Open the keyboard on a small iPhone, type into the field, and check that the user can confirm or cancel. |
| The highlight clips part of a card or includes the card beside it. | Compare the highlight and its pointer with the rendered controls on each affected step. |
| The wrong tap advances the guide. | Try both the intended action and a nearby control. Check which input the app receives and when the guide advances. |
| The next step appears before its screen is ready. | Follow the actual navigation transition and check when the target becomes visible and usable. Test the return path if the guide supports going back. |
| A replay picks up stale practice data. | Check what happens to practice data after completion, skip, or interruption, then replay the guide. Track completed guides separately from the current run. |

## Use

The workflow lives in [SKILL.md](skills/ios-guide-workflow/SKILL.md). Place the `skills/ios-guide-workflow` folder in a skill directory supported by your environment.

Open your iOS project and describe what you want the guide to do. For example:

- **Build a guide.** Walk a new user through setting their first reminder. Let them enter a label and pick a time before continuing.
- **Explain a feature.** Walk users through this chart. Show what it measures and how the date filter changes the result.
- **Fix a step.** When the keyboard opens, the callout covers Save. Fix the layout and retest typing, saving, and cancelling on a small iPhone.

The workflow reads the project and its previous decisions before asking questions. It asks only about choices that affect the guide, such as when to show it, what advances a step, and what happens to practice data. It saves those decisions and later corrections in the target project so the next revision can pick up where you left off.

## Validation status

The initial release went through manifest and link checks, a check for project-specific content, and an independent package review. Nine synthetic scenarios tested the workflow's recommendations. Each app still needs its own build, interaction, accessibility, and human acceptance checks.

## License

[MIT](LICENSE).
