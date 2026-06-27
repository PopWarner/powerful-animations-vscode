# Known Issues

This page tracks known bugs and limitations in the current release. Check here before opening a new issue.

---

## Current release (0.1.0)

### SVG Preview

**Complex SVG filters may render differently than Power Apps**
The preview panel uses VS Code's built-in webview browser engine. Complex `<filter>` effects, non-standard SVG features, or browser-specific rendering behavior may cause the preview to look slightly different from what Power Apps renders. The SVG itself is not modified. This is a rendering environment difference.

**Large SVG files may have a slight preview delay**
Very large SVGs (especially those with many elements or complex paths) may take a moment to update in the preview panel after edits. This is a known performance limitation with the current rendering approach.

### Create Dynamic SVG Variable

**Multi-line selections require confirmation**
If you select text that spans multiple lines, the extension will ask you to confirm before continuing. This is intentional. Multi-line selections are unusual for single variable values and the prompt exists to prevent accidental replacements.

**Power Fx expressions are not valid SVG**
Once Power Fx variable expressions are inserted, the resulting file is no longer a valid standalone SVG. The VS Code SVG validator (if you have one installed) may show errors. This is expected. Use the **Create Working Copy** option to preserve your original SVG.

---

## Limitations by design

- The `With()` variable substitution in the preview only works with literal default values. Variables pointing to other variables or formulas are not resolved.
- The extension does not validate SVG syntax. Use a dedicated SVG linter or the browser developer tools for validation.
- The Animation Gallery is not yet available. The panel shows a coming-soon placeholder.

---

## Not listed here?

If you hit something that is not on this page, [open an issue](https://github.com/PopWarner/powerful-animations-vscode/issues/new?template=bug_report.md). Please include:

- VS Code version
- Operating system
- Steps to reproduce
- What you expected to happen
- What actually happened
