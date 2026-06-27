# FAQ

## General

### Is this extension free?

Yes. Powerful Animations is free to install and use.

### Does it work with any SVG, or only Power Apps SVGs?

It works with any SVG file. The Power Apps-specific commands (Prepare SVG, Create Dynamic SVG Variable) are there when you need them, but the preview and playback controls work with any SVG regardless of what it is for.

### Does it require an internet connection?

No. Everything runs locally in VS Code. There are no external services, no API calls, no accounts.

---

## SVG Preview

### The preview button is not showing up in my editor toolbar

The preview button only appears when VS Code recognizes the file as SVG. Try:

1. Check the language mode shown in the bottom-right status bar — it should say **SVG**
2. If it shows **Plain Text** or something else, click it and search for SVG to set it manually
3. Save the file with a `.svg` extension if it does not already have one

The extension sets SVG language mode automatically when you open `.svg` files. If you created the file in VS Code as a new untitled file, set the language mode before pasting your SVG content.

### The preview is blank

- Make sure the SVG has a `viewBox` or explicit `width`/`height` attributes
- Check the VS Code Developer Tools console (`Help → Toggle Developer Tools`) for any errors
- Try the SVG in a browser — if it is blank there too, the SVG itself may have an issue

### My With() formula preview is not substituting variable values

The extension reads defaults from the `With` block at the top of the formula. Make sure:

- The file starts with `With(` followed by the variable block
- Variable defaults are literal values (not other formulas or variables)
- The variable names in the `With` block match the variable names used in the SVG string

---

## Power Apps Commands

### The Prepare SVG command adds `EncodeUrl(...)` — do I need that?

Yes. Power Apps Image controls require SVG content to be URL-encoded. Without `EncodeUrl`, special characters in the SVG (angle brackets, quotes, hashes, spaces) will break the formula.

### Can I prepare only part of an SVG?

Yes. Select the text you want to convert before running **Prepare SVG for Power Apps**. If nothing is selected, the full document is used.

### The single-quote conversion is changing quotes inside attribute values I want to keep

The **Convert to Single Quotes** command converts all double quotes in the selected text (or full document). Select only the portion you want to convert if you need finer control.

### What is the difference between the two options in Create Dynamic SVG Variable?

| Option | What it does |
| --- | --- |
| **Create Working Copy and Insert Variable** | Opens a new file with the dynamic formula. Your original SVG stays untouched. Recommended starting point. |
| **Insert Variable in Current Document** | Updates the active file directly. Use this when you are already working in a dynamic SVG draft and want to add another variable. |

---

## Settings

### What does `useThemeColors` actually change?

It swaps the purple-to-orange gradient on the SVG Tools command cards in the sidebar for your active VS Code theme's accent color. Everything else stays the same.

### What are preview features?

Preview features are experimental capabilities that may change, break, or be removed before they ship in a stable release. Enable `showPreviewFeatures` if you want early access and are comfortable with that tradeoff.

---

## Still stuck?

[Open an issue](https://github.com/PopWarner/powerful-animations-vscode/issues/new?template=bug_report.md) and describe what is happening. Include your VS Code version and OS.
