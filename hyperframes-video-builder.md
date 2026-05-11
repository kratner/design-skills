# HyperFrames Video Builder Skill

## Purpose

Generate production-quality HTML5 video content using HyperFrames—deterministic, responsive, exportable as MP4/WebM/MOV. Build landing page teasers, product demos, social ads, testimonial videos, animated explainers, and more. All videos render with precise timing, seekable timelines, and pixel-perfect frame control.

## How to Use

```
/use hyperframes-video-builder

Describe your video:
1. What type of video? (landing page teaser, product demo, social ad, testimonial, explainer, etc.)
2. Duration? (seconds)
3. Key message or narrative? (headline, flow, talking points)
4. Visual style? (brand colors, animation style, any reference videos)
5. Audio? (voiceover, music, silent)
```

## Video Anatomy (HyperFrames Basics)

All HyperFrames videos are HTML5 compositions:

```html
<!-- composition.html -->
<!DOCTYPE html>
<html>
  <head>
    <meta name="duration" content="10">
    <meta name="fps" content="30">
    <title>My Video</title>
    <style>
      body { background: #fff; margin: 0; overflow: hidden; }
      video { width: 100%; height: 100%; }
    </style>
  </head>
  <body>
    <!-- Layers, text, images, video, animations -->
    <div data-hf-seek="0" data-hf-duration="3">
      <!-- Frame 0-3 seconds -->
    </div>

    <script>
      // Timeline control via hf-seek events
      document.addEventListener('hf-seek', (e) => {
        // e.detail.time = current playhead (0-duration)
      });
    </script>
  </body>
</html>
```

## Key Concepts

### 1. **Seekable Timeline**
HyperFrames videos are frame-accurate, seekable to any timestamp. Use `data-hf-seek` + `data-hf-duration` attributes to control what's visible at which frame.

```html
<!-- This element is visible 0-3 seconds -->
<div data-hf-seek="0" data-hf-duration="3">
  <h1>Intro Text</h1>
</div>

<!-- This element is visible 3-6 seconds -->
<div data-hf-seek="3" data-hf-duration="3">
  <h2>Next Scene</h2>
</div>
```

### 2. **Animation Timing**
Use CSS animations or JavaScript to drive motion. HyperFrames will render every frame precisely.

```html
<style>
  @keyframes slideIn {
    from { transform: translateX(-100%); }
    to { transform: translateX(0); }
  }

  .hero {
    animation: slideIn 1s ease-out forwards;
    animation-delay: 0.5s;
  }
</style>
```

### 3. **Responsive Canvas**
HyperFrames renders at 1920×1080 (16:9) by default, but you can customize dimensions in the `<meta>` tags.

```html
<meta name="width" content="1920">
<meta name="height" content="1080">
<meta name="fps" content="30">
```

### 4. **Media Assets**
Embed images, videos, audio, fonts. All must be local files or data URIs (no external URLs in render).

```html
<img src="./assets/logo.png" alt="Logo">
<video src="./assets/background.mp4" autoplay muted loop></video>
```

## Common Video Types & Patterns

### Landing Page Teaser (15-30 sec)
- Hero title + subheading (0-2s)
- Key benefits scroll/fade in (2-10s)
- CTA button highlight (10-15s)
- Social proof stats (15-20s)
- Final CTA with fade (20-30s)

```html
<div data-hf-seek="0" data-hf-duration="2">
  <h1 class="fade-in">Your Headline Here</h1>
</div>
<div data-hf-seek="2" data-hf-duration="8">
  <div class="benefits slide-up">
    <div>Benefit 1</div>
    <div>Benefit 2</div>
    <div>Benefit 3</div>
  </div>
</div>
<div data-hf-seek="10" data-hf-duration="5">
  <button class="cta pulse">Get Started</button>
</div>
```

### Product Demo (30-60 sec)
- Product hero shot (0-3s)
- Problem statement (3-8s)
- Feature walkthrough with screen recordings (8-40s)
- Results/ROI (40-50s)
- CTA (50-60s)

### Social Ad (6-15 sec)
- Hook: Grab attention in first 1s (0-1s)
- Problem: Show pain point (1-3s)
- Solution: Demonstrate benefit (3-8s)
- CTA: Call to action (8-15s)

**Key for social:** Motion, text overlays, bold colors. Assume no audio (captions essential).

### Testimonial Video (20-45 sec)
- Guest intro + headshot (0-3s)
- Quote/story (voiceover + text) (3-35s)
- Results: ROI/metrics (35-40s)
- Brand logo + CTA (40-45s)

### Explainer/Educational (60-180 sec)
- Intro scene (0-5s)
- Problem setup (5-15s)
- Solution walkthrough (15-50s) — complex, multi-step
- Recap + CTA (50-60s)

Best for: Complex concepts, tutorials, how-to videos.

## Animation Patterns

### Fade In
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
.element { animation: fadeIn 0.8s ease-out forwards; }
```

### Slide In (Left to Right)
```css
@keyframes slideInRight {
  from { transform: translateX(-100%); opacity: 0; }
  to { transform: translateX(0); opacity: 1; }
}
```

### Scale + Fade (Entrance)
```css
@keyframes scaleIn {
  from { transform: scale(0.8); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}
```

### Text Character Animation
```html
<div class="text-reveal">
  <span data-hf-seek="1" data-hf-duration="2">H</span>
  <span data-hf-seek="1.1" data-hf-duration="2">e</span>
  <span data-hf-seek="1.2" data-hf-duration="2">l</span>
  <!-- etc -->
</div>
```

### Pulse / Attention
```css
@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.1); }
}
.element { animation: pulse 1s infinite; }
```

## HyperFrames CLI Workflow

```bash
# Install HyperFrames (one-time)
npm install -g @hyperframes/cli

# Initialize a new video project
hyperframes init my-video

# Preview in browser (localhost:3000)
hyperframes preview composition.html

# Lint composition for errors
hyperframes lint composition.html

# Render to MP4
hyperframes render composition.html --output video.mp4

# Render to WebM (better for web)
hyperframes render composition.html --output video.webm --codec vp9

# Render multiple formats
hyperframes render composition.html --formats mp4,webm,mov
```

## Design Integration

### Use Power Design Principles
- **Rule 2 (Simplicity)**: Limit on-screen elements. Max 3 key messages per scene.
- **Rule 4 (White Space)**: Don't clutter. Leave breathing room in animations.
- **Rule 12 (Consistency)**: Use same brand colors, fonts, timing throughout.
- **Rule 15 (Alignment)**: Snap all elements to invisible grid.
- **Rule 19 (Accessibility)**: Add captions for all voiceover. Test on muted.

### Use Design Tokens
If building branded videos, pull colors, fonts, spacing from your DESIGN.md:

```css
:root {
  --color-primary: #2563eb;
  --color-secondary: #1e40af;
  --font-display: 'Inter', sans-serif;
  --spacing: 24px;
}

h1 { color: var(--color-primary); font-family: var(--font-display); }
```

### Use Layout Validator Principles
- **F-Pattern**: Guide eye from top-left → down → right → CTA
- **Whitespace**: ≥40% empty space so viewer can breathe
- **Grid Alignment**: All positions snap to 8px or 16px increments

## Common Gotchas & Fixes

### 1. **Audio Sync Issues**
If voiceover drifts, you've likely misaligned animation timing. Verify:
```html
<!-- Audio plays 0-30s -->
<audio src="voiceover.mp3" data-hf-seek="0" data-hf-duration="30"></audio>

<!-- Text must match voiceover timing exactly -->
<div data-hf-seek="0" data-hf-duration="5">First sentence (0-5s)</div>
<div data-hf-seek="5" data-hf-duration="5">Second sentence (5-10s)</div>
```

### 2. **Animation Jank**
If animations stutter, avoid:
- Heavy CSS shadows
- Unoptimized images (compress to <500KB)
- Too many simultaneous animations (max 5 per frame)

### 3. **Text Readability**
On video, text must be **large** and **high contrast**. Test:
- Minimum font size: 32px (for 1920×1080)
- Contrast ratio: ≥4.5:1 (WCAG AA)
- Sans-serif fonts only (serif doesn't render well in video)

### 4. **Render Failures**
If `hyperframes render` fails:
```bash
# Check composition for errors
hyperframes lint composition.html

# Verify all assets are local (no external URLs)
# Verify all image paths are correct
# Verify <meta> tags are valid (fps, duration, dimensions)
```

## Example: 15-Second Social Ad

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="duration" content="15">
    <meta name="fps" content="30">
    <meta name="width" content="1080">
    <meta name="height" content="1920">
    <title>Social Ad</title>
    <style>
      * { margin: 0; padding: 0; box-sizing: border-box; }
      body {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
        font-family: 'Inter', sans-serif;
        color: #fff;
      }

      .container {
        text-align: center;
        padding: 40px;
      }

      h1 {
        font-size: 80px;
        font-weight: 700;
        line-height: 1.2;
        margin-bottom: 20px;
      }

      p {
        font-size: 48px;
        margin-bottom: 40px;
        opacity: 0.9;
      }

      button {
        background: #fff;
        color: #667eea;
        border: none;
        padding: 24px 60px;
        font-size: 40px;
        font-weight: 700;
        border-radius: 12px;
        cursor: pointer;
      }

      @keyframes fadeIn {
        from { opacity: 0; }
        to { opacity: 1; }
      }

      @keyframes slideUp {
        from { transform: translateY(60px); opacity: 0; }
        to { transform: translateY(0); opacity: 1; }
      }

      .fade-in { animation: fadeIn 0.8s ease-out forwards; }
      .slide-up { animation: slideUp 1s ease-out forwards; }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- Hook: 0-1s -->
      <div data-hf-seek="0" data-hf-duration="1">
        <h1 class="fade-in">Stop Wasting Time</h1>
      </div>

      <!-- Problem: 1-4s -->
      <div data-hf-seek="1" data-hf-duration="3">
        <p class="slide-up">Repetitive tasks killing your productivity?</p>
      </div>

      <!-- Solution: 4-8s -->
      <div data-hf-seek="4" data-hf-duration="4">
        <p class="slide-up">Automate everything in minutes</p>
      </div>

      <!-- CTA: 8-15s -->
      <div data-hf-seek="8" data-hf-duration="7">
        <button class="fade-in">Learn More</button>
      </div>
    </div>
  </body>
</html>
```

Render:
```bash
hyperframes render composition.html --output ad.mp4
```

## When to Use HyperFrames

**Best for:**
- Social ads (Instagram, TikTok, YouTube shorts)
- Product demos with precise timing
- Landing page animations (animated hero, feature showcase)
- Testimonial compilations
- Educational explainers
- Animated infographics with data

**Not ideal for:**
- Multi-camera narrative films (use Premiere/Final Cut Pro)
- Real-time interactive content (use web app instead)
- Unscripted footage (needs live recording)

## Integration with Other Design Skills

- **power-design-audit**: Validate final video against 10 design principles before rendering
- **layout-validator**: Check F-pattern eye flow, whitespace, alignment in key frames
- **color-system-builder**: Generate consistent color palette for video branding
- **design-extract**: Study competitor video styles from brand sites

## Resources

- **HyperFrames Docs**: https://hyperframes.ai/docs
- **CLI Reference**: `hyperframes --help`
- **Examples**: See HyperFrames repo for sample compositions
- **GSAP for Animation**: Use GSAP timelines in HyperFrames for complex motion (see gsap skill)

---

**Output includes:** Production-ready HTML5 composition, timing cues, animation code, and render commands to export MP4/WebM/MOV.

**Next steps after using this skill:**
1. Review generated composition in browser (`hyperframes preview`)
2. Adjust timing/animations as needed
3. Test on muted (captions readable?)
4. Render to target format (`hyperframes render`)
5. Upload to social/web platform
