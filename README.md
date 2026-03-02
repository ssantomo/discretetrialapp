[README.md](https://github.com/user-attachments/files/25692291/README.md)
# Discrete Trial (iOS)

Discrete Trial is an iOS app for running paperless ABA target sessions with built-in data collection, image-based tacting, and export tools.

## Overview

The app organizes language and learning targets into folder-based libraries. Clinicians can run sessions directly on iPhone/iPad, collect trial data, review summaries, and export results.

## Core Features

- Home screen with folder-based target libraries
- Written target lists (50 targets per folder where applicable)
- Tacting Objects and Tacting Actions with image viewing
- Generalization mode for tacting targets (3 images per target)
- Object Identification and Action Identification array trials (2/3/6/10)
- Correct/Incorrect data collection at target level
- Data summaries (correct totals, percentage, probed counts)
- Export data as `.pdf`, `.csv`, or `.jpg`
- Data persists while app remains open and resets when app is fully closed/restarted

## Home Screen Folders

1. Following Directions
2. Motor Imitation
3. Object Imitation
4. Imitation of Fine Motor Skills
5. Echoics of Sounds and Words
6. Tacting Objects
7. Tacting Actions
8. Object Identification
9. Action Identification
10. Intraverbals
11. WH-Questions
12. Function
13. Feature
14. Class

## Data Collection Notes

- Function, Feature, and Class support separate data collection for both:
  - Prompt target
  - Reverse target
- WH-Questions are organized by type in the UI:
  - Who
  - What
  - Where
  - When
  - Why
- Object/Action Identification tracks summaries by array size:
  - Array of 2, 3, 6, 10

## Photo Resources

Main image folder:

`ABATargetLibraryiOS/ABATargetLibraryApp/Resources/Photos`

For tacting generalization, each base target should have:

- Base image (example: `obj_apple.jpg`)
- `*_gen_photo` variant
- `*_gen_cartoon` variant

## Build Requirements

- Xcode 15+
- iOS target configured in project settings
- iOS Simulator runtime installed (if using simulator)

## Run the App

1. Open `DiscreteTrialApp.xcodeproj` in Xcode.
2. Select an iOS simulator or a connected iPhone/iPad.
3. Build and run.

## Encryption Declaration (App Store)

The project is configured with:

- `ITSAppUsesNonExemptEncryption = NO`

This is set in the Xcode project build settings (generated Info.plist key).

## Project Structure

- `ABATargetLibraryiOS/ABATargetLibraryApp.swift` - main app UI and data logic
- `ABATargetLibraryiOS/ABATargetLibraryApp/Resources/Photos` - target images
- `DiscreteTrialApp.xcodeproj` - Xcode project
- `DiscreteTrialClip/` - App Clip target files

## Notes

- This app is designed to run on iPhone and iPad when target device family is set to Universal (`iPhone, iPad`).
- If newly added images do not appear, clean build folder and reinstall app to refresh bundled resources.
