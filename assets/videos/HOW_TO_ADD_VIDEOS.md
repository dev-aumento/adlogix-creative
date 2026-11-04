# How to Provide & Add UGC Videos to AdLogix Portfolio

This guide explains how to add, replace, or customize User-Generated Content (UGC) videos and Reels on the AdLogix web portfolio.

---

## 1. Quick Video Specifications

| Property | Recommended Specification |
|---|---|
| **Format** | `.mp4` (H.264 / AAC) or `.webm` |
| **Orientation** | **Vertical 9:16** (portrait mode) |
| **Resolution** | **1080 x 1920 px** (FHD) or **720 x 1280 px** (HD) |
| **Duration** | **15 to 45 seconds** (optimal for ad hooks & conversion) |
| **File Size** | **Under 10 MB - 15 MB** per video (for instant web loading) |
| **Audio** | Clear voiceover / hook with ambient sound (starts muted by default in web browsers) |

---

## 2. Three Ways to Provide Your Videos

### Option A: Direct Local Drop (Easiest)
1. Export or download your 9:16 MP4 video files.
2. Rename or save them into this folder:
   ```text
   assets/videos/
   ├── ugc_reel_01.mp4   (e.g., E-Commerce & D2C Unboxing)
   ├── ugc_reel_02.mp4   (e.g., Cafe & Restaurant Foodie ASMR)
   ├── ugc_reel_03.mp4   (e.g., Real Estate Luxury Walkthrough)
   ├── ugc_reel_04.mp4   (e.g., Salon & Glow Transformation)
   ├── ugc_reel_05.mp4   (e.g., Retail & Fashion Styling)
   └── ugc_reel_06.mp4   (e.g., Manufacturing Behind-the-Scenes)
   ```
3. If you want custom file names, simply update the `videoSrc` path in `index.html` under `const ugcReels = [...]`.

---

### Option B: Cloud Link (Google Drive / WeTransfer / Dropbox)
If your videos are on your phone or camera:
1. Upload the vertical videos to a **Google Drive folder** or **Dropbox** / **WeTransfer**.
2. Set the link sharing permission to: **"Anyone with link can view / download"**.
3. Share the link with us. We will:
   - Check and optimize the aspect ratio to 9:16
   - Compress the video size for blazing fast loading
   - Add the custom hook, creator tag, and ROAS metrics to your portfolio!

---

### Option C: Direct CDN or Hosted Video URL
If your videos are hosted on **Cloudflare Stream**, **Vimeo**, **AWS S3**, or **Supabase**:
- You can directly paste the raw `.mp4` streaming URL into `videoSrc` in `index.html`:
  ```javascript
  videoSrc: "https://your-cdn.com/videos/brand_reel_01.mp4"
  ```

---

## 3. How to Customize Creator Name, Hook & Metrics

In `index.html`, find the `ugcReels` array near the bottom of `<script>`:

```javascript
{
  id: "ugc-1",
  title: "Viral Unboxing & First Impression",
  industry: "E-Commerce",
  brand: "LuxeSkin Organic D2C",
  creator: "@alyssa_glows",
  creatorFollowers: "420K",
  hookType: "⚡ 3s Pattern Interrupt Hook",
  hookQuote: "“Stop throwing money away on chemical serums...”",
  duration: "0:24",
  roas: "5.4x ROAS",
  views: "1.8M Views",
  ctr: "3.9% CTR",
  cpaReduction: "-42% CPA",
  videoSrc: "assets/videos/ugc_reel_01.mp4",
  poster: "assets/projects/shopify_dashboard.png"
}
```

Edit any of the text fields, save the file, and refresh your browser!
