# Image Insertion Guide

Welcome! This guide explains how to easily add images to your portfolio. All photo slots are pre-formatted and ready for your images.

## Quick Start

### 1. **Prepare Your Images**
- **Size**: Optimized for 16:9 aspect ratio (1600×900px or similar)
- **Format**: JPG, PNG, or WebP recommended
- **Location**: Create an `img/` folder at the root of your repository and upload images there
- **Naming**: Use descriptive names (e.g., `textron-hinged-door.jpg`, `bipropellant-injector.jpg`)

### 2. **Find Your Photo Slots**

All photo slots are marked in the HTML with this structure:
```html
<div class="photo-slot">
  <span class="fig">Fig. 01</span>
  <span class="instr">+ Add Photo</span>
</div>
```

### 3. **Add an Image**

Replace the placeholder with an `<img>` tag. Example:

**Before:**
```html
<div class="photo-slot">
  <span class="fig">Fig. 01</span>
  <span class="instr">+ Add Photo</span>
</div>
```

**After:**
```html
<div class="photo-slot">
  <img src="img/textron-hinged-door.jpg" alt="Textron MX4 hinged door design from CAD">
  <span class="fig">Fig. 01</span>
  <span class="instr">+ Add Photo</span>
</div>
```

### 4. **The CSS Handles the Rest**

When an image is present, the CSS automatically:
- ✅ Hides the "Fig. XX" and "+ Add Photo" labels
- ✅ Crops the image to fit the 16:9 slot perfectly
- ✅ Removes the dashed border
- ✅ Displays the image smoothly

## Photo Slots by Page

### **index.html** (Home Page - 5 feed items)
- Fig. 01: Bipropellant Rocket Engine
- Fig. 02: Carbon Fiber Fuselage — PADA
- Fig. 03: MX4 & 660 Electrification Doors
- Fig. 04: Blended Wing Body vs. RANS CFD
- Fig. 05: Compound Delta Wing CFD

### **build.html** (Build Projects - 5 project sheets)
- Fig. 01: Textron GSE — Cartersville, GA
- Fig. 02: Bipropellant Rocket Engine
- Fig. 03: Fin Can & Airframe Fit
- Fig. 04: Powered Autonomous Delivery Aircraft (PADA)
- Fig. 05: Aerodynamic Surface-Treatment Testbed

### **research.html** (Research - 4 research sheets)
- Fig. 01: Blended Wing Body vs. RANS CFD
- Fig. 02: Compound Delta Wing CFD
- Fig. 03: Control Surface Validation — "Bird" UAV
- Fig. 04: Forward-Facing Cavity PIV Replication

### **about.html** (About Me - No photo slots)
*This page doesn't have photo slots, but you can add a profile image if needed.*

## Image Best Practices

### Recommended Dimensions
| Type | Aspect Ratio | Suggested Size |
|------|--------------|----------------|
| Project photos | 16:9 | 1600×900px |
| CAD renderings | 16:9 | 1600×900px |
| Test setup photos | 16:9 | 1600×900px |
| Finished products | 16:9 | 1600×900px |

### Alt Text
Always include descriptive `alt` text for accessibility and SEO:
```html
<img src="img/rocket-engine.jpg" alt="N2O/ethanol bipropellant engine assembly on test stand">
```

### File Size
- Aim for **50–150 KB** per image for fast loading
- Use tools like [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/) to compress

### Color Grading
Your portfolio uses a clean, professional color palette:
- **Black background**: #1F1F1F
- **Red accent**: #B20000
- **Light gray background**: #F7F7F7

Consider images that complement this scheme (crisp lighting, high contrast).

## Folder Structure

```
Andrew-Marion/
├── index.html
├── about.html
├── build.html
├── research.html
├── style.css
├── img/
│   ├── textron-hinged-door.jpg
│   ├── bipropellant-engine.jpg
│   ├── pada-fuselage.jpg
│   ├── bwb-cfd.jpg
│   └── delta-wing-cfd.jpg
└── IMAGE_GUIDE.md (this file)
```

## Editing Steps

1. **Upload images** to the `img/` folder
2. **Edit each HTML file** and add `<img>` tags to the photo slots
3. **Commit and push** to GitHub
4. **GitHub Pages** will automatically deploy your updated portfolio

## Example: Complete Edit

**build.html** — Adding the Textron door image:

```html
<!-- BEFORE -->
<div class="sheet reveal" id="textron">
  <div class="photo-slot">
    <span class="fig">Fig. 01</span>
    <span class="instr">+ Add Photo</span>
  </div>
  <div class="sheet-top">
    <span>Textron GSE — Cartersville, GA</span>
    <span>Jun–Aug 2026</span>
  </div>
  ...

<!-- AFTER -->
<div class="sheet reveal" id="textron">
  <div class="photo-slot">
    <img src="img/textron-hinged-door.jpg" alt="CAD rendering of hinged door for MX4 electric baggage tractor">
    <span class="fig">Fig. 01</span>
    <span class="instr">+ Add Photo</span>
  </div>
  <div class="sheet-top">
    <span>Textron GSE — Cartersville, GA</span>
    <span>Jun–Aug 2026</span>
  </div>
  ...
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Image doesn't show | Check the file path in `src=""` — should be `img/filename.jpg` |
| Image looks blurry/cropped | Ensure image is at least 1600×900px; CSS uses `object-fit:cover` |
| Placeholder still shows | Make sure the `<img>` tag is inside the `.photo-slot` div |
| File too large | Compress using online tools before uploading |

---

**Questions?** Refer back to the CSS in `style.css` — the `.photo-slot` and `.feed-photo` classes handle all the styling automatically!
