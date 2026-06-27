# Change Log

All notable changes to the "powerful-animations" extension are documented in this file.

## [0.1.0] - 2026-06-25

The big one. This release introduces the SVG Preview panel, a completely redesigned sidebar, and a pile of quality-of-life improvements for the dynamic variable workflow.

### Added

#### SVG Preview Panel

- Added SVG Preview panel that opens beside the active editor and updates live as you type
- Added Studio Bar with playback controls: Restart (↺), Play/Pause (⏸/▶), and Loop toggle (⟳)
- Loop toggle waits for the current animation cycle to finish before stopping, so nothing gets cut off mid-spin
- Added smart Power Apps formula detection: the preview strips the `EncodeUrl` wrapper and renders the SVG directly, even from formula files
- Added `With()` variable substitution in the preview: variable defaults from the `With` block are substituted into the SVG before rendering, so the animation runs with real values
- Added animated gradient strip on the Studio Bar (breathes gently at rest, shimmers on hover)
- Added glassmorphism Studio Bar that fades to 40% opacity when idle and snaps to full opacity on hover

#### Sidebar

- Added SVG Tools panel with three command cards for one-click access to the most-used commands
- Added Animation Gallery panel (coming soon state with category preview pills)
- Added Featured Video panel
- Added `powerful-animations.useThemeColors` setting to replace brand colors with the active VS Code theme accent color
- Added `powerful-animations.showPreviewFeatures` setting to opt into preview features

#### SVG Language Support

- Added automatic SVG language detection: SVG files now set the correct language mode on open so the editor toolbar preview button always appears
- Output files from Prepare SVG and Create Dynamic SVG Variable now open as SVG language so the preview button is immediately available

### Changed

- Output files from the Prepare SVG and Create Dynamic SVG Variable commands now open as SVG language instead of plain text
- Updated SVG Tools sidebar with grouped command cards using Powerful Animations brand colors (purple to orange gradient)
- Improved Animation Gallery panel copy to be platform-agnostic

### Fixed

- Fixed SVG files sometimes opening as plain text instead of SVG language mode

## [0.0.6]

- Added early dynamic variable command experiments
- Fixed extension icon filename from `powrfulanimations.png` to `powerfulanimations.png`

## [0.0.5]

- Added SVG preparation for Power Apps Image controls
- Added double quote to single quote conversion
