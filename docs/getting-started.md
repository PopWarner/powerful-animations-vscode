# Getting Started

## Install

Search **Powerful Animations** in the VS Code Extensions panel, or install from the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=WarnerDigital.powerful-animations).

After installing, the Powerful Animations icon appears in the Activity Bar on the left side of VS Code.

---

## Your first five minutes

### 1. Open an SVG file

Open any `.svg` file. VS Code will automatically detect it and:

- Add the **Preview SVG** button (the eye icon) to the editor toolbar
- Make the Powerful Animations commands available in the right-click context menu

### 2. Preview it live

Click the preview icon (👁) in the top-right of the editor. A live preview panel opens beside your file and updates as you type. If the SVG is animated, it plays immediately.

<!-- Screenshot: SVG Preview panel open in split view beside an SVG file, Studio Bar visible at the bottom -->
<!-- Drop file at: public-repo/images/getting-started-preview-panel.png -->
![SVG Preview panel open beside an SVG file in split view](../images/getting-started-preview-panel.png)

### 3. Prepare it for Power Apps

Right-click in the SVG editor and choose **Powerful Animations: Prepare SVG for Power Apps**. The extension converts the SVG into a formula you can paste directly into a Power Apps Image control:

```powerfx
"data:image/svg+xml;utf8," & EncodeUrl("<svg ...>...</svg>")
```

The formula is copied to your clipboard and opened in a new file for review.

### 4. Make a value dynamic

Select a hardcoded value in your SVG — a color like `#ff0000`, a duration like `1500ms`, anything you might want to control from Power Apps. Right-click and choose **Powerful Animations: Create Dynamic SVG Variable**.

Name your variable, choose whether to create a working copy or update the current document, and pick **With() formula** if you want defaults baked in. The extension replaces the selected value with a Power Fx expression and copies the result to your clipboard.

<!-- Screenshot: Create Dynamic SVG Variable QuickPick showing the two workflow options -->
<!-- Drop file at: public-repo/images/getting-started-dynamic-variable.png -->
![Create Dynamic SVG Variable QuickPick showing workflow options](../images/getting-started-dynamic-variable.png)

---

## Sidebar panels

Click the Powerful Animations icon in the Activity Bar to open the sidebar.

<!-- Screenshot: Full Powerful Animations sidebar showing all three panels -->
<!-- Drop file at: public-repo/images/getting-started-sidebar.png -->
![Powerful Animations sidebar showing SVG Tools, Animation Gallery, and Featured Video panels](../images/getting-started-sidebar.png)

| Panel | What it does |
| --- | --- |
| **SVG Tools** | One-click buttons for the three most-used commands |
| **Animation Gallery** | Coming soon — a free library of copy-ready SVG animations |
| **Featured Video** | A curated walkthrough video, updated as new features ship |

---

## Next steps

- Read the full command documentation on the [VS Code Marketplace listing](https://marketplace.visualstudio.com/items?itemName=WarnerDigital.powerful-animations)
- Check [FAQ](faq.md) for common questions
- Check [Known Issues](known-issues.md) if something is not behaving as expected
