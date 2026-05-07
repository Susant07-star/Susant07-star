# 🚀 Susant's GitHub Profile — Full Improvement Plan
> **Profile:** https://github.com/Susant07-star  
> **Last updated:** April 29, 2026  
> **README file:** `E:\GitHub\Susant07-star\README.md`

---

## ✅ Already Done
- [x] Epic animated Profile README with typing header, wave banners
- [x] About Me section (Python class style)
- [x] Tech Stack skill icons
- [x] Featured project repo cards (ROVA, board-exam-countdown-2083, Jarvis-AI, HourForge)
- [x] Project showcase table with descriptions
- [x] Live GitHub Stats card, Streak counter, Top Languages, Activity Graph
- [x] GitHub Trophies section
- [x] Snake animation (generic — needs Actions fix)
- [x] Footer wave + profile view counter
- [x] Fixed typing animation width/speed/cropping issues
- [x] Swapped Go-Green with board-exam-countdown-2083

---

## 🔴 HIGH PRIORITY — Do These First

### 1. 🐍 Fix Snake Animation (YOUR Contribution Grid)
> **Status:** ✅ Done (pending push/run)
> **Time:** ~10 minutes  
> **Why:** Currently uses a generic/sample snake. Needs GitHub Actions to generate a snake from YOUR actual contribution squares.

**Steps to do it:**
1. Create file: `E:\GitHub\Susant07-star\.github\workflows\snake.yml`
2. Add this content:
```yaml
name: Generate Snake Animation

on:
  schedule:
    - cron: "0 */12 * * *"  # runs every 12 hours
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 10
    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
3. Push the file to GitHub
4. Go to: `https://github.com/Susant07-star/Susant07-star/actions` → Run the workflow manually
5. Update the snake URLs in README.md from:
   - `https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg`
   - to: `https://raw.githubusercontent.com/Susant07-star/Susant07-star/output/github-snake-dark.svg`

---

### 2. 📌 Pin Top 6 Repos on Profile
> **Status:** ⏳ Not done  
> **Time:** 5 minutes (manual on GitHub)  
> **Why:** Visitors see pinned repos immediately. Nothing is pinned right now.

**Steps:**
1. Go to https://github.com/Susant07-star
2. Click "Customize your pins"
3. Pin these 4 repos (in order):
   - `Jarvis-AI`
   - `PROTO-X-ROVA`
   - `HourForge`
   - `board-exam-countdown-2083`

---

### 3. 🧑 Fill in GitHub Profile Sidebar
> **Status:** ⏳ Not done  
> **Time:** 5 minutes (manual on GitHub)  
> **Why:** Your sidebar is completely blank — looks unprofessional

**Steps:**
1. Go to: https://github.com/settings/profile
2. Add these fields:
   - **Bio:** `Student Developer | Robotics & AI | Building for Nepal 🇳🇵`
   - **Location:** `Nepal`
   - **Website:** *(your Netlify countdown URL if you have one)*
   - **Profile picture:** Add a real photo or a cool avatar

---

### 4. 🏷️ Add Topics/Tags to Each Repo
> **Status:** ⏳ Not done  
> **Time:** 10 minutes total  
> **Why:** Makes repos discoverable in GitHub search & trending

**Go to each repo → gear icon next to "About" → add topics:**

| Repo | Suggested Topics |
|---|---|
| PROTO-X-ROVA | `robotics`, `raspberry-pi`, `voice-control`, `opencv`, `python`, `ai`, `arduino` |
| board-exam-countdown-2083 | `nepal`, `neb`, `countdown`, `javascript`, `education`, `netlify` |
| TSA-IT-Club-website | `school`, `club`, `website`, `html`, `nepal` |

---

## 🟡 MEDIUM PRIORITY

### 5. 📝 Individual Repo READMEs
> **Status:** ⏳ Not done  
> **Why:** Every repo currently has a weak or no README. A great README = credibility + stars.

**Repos that need READMEs (priority order):**

#### A. `PROTO-X-ROVA` — Most impressive project
Should include:
- Project banner image / demo GIF
- Hardware components list (motors, RPi, sensors)
- Architecture diagram
- Installation steps
- Voice commands list
- Demo video link
- Tech stack badges

#### B. `board-exam-countdown-2083`
Should include:
- Screenshot of the website
- Live demo link (Netlify URL)
- Features list
- How to use
- Subjects covered

---

### 6. 🖼️ Social Preview Images (OG Images)
> **Status:** ⏳ Not done  
> **Why:** When you share a repo link on WhatsApp/Twitter/Discord, it shows a custom image

**Steps:**
1. I can generate a custom preview image for each repo
2. Go to: `Repo → Settings → Social preview → Upload image`
3. Recommended size: **1280 × 640px**

---

### 7. 🌐 Portfolio Website Link
> **Status:** ⏳ Not done  
> **Why:** A portfolio link on your GitHub profile adds a ton of credibility

**Option:** I can build you a simple one-page portfolio website and deploy it on Netlify for free. It would include:
- Your projects showcase
- Skills
- Contact section
- Link back to GitHub

---

## 🟢 NICE TO HAVE

### 8. 📋 `.github/` Folder Templates
> Add to each repo for professional open-source look:
- `CONTRIBUTING.md`
- `LICENSE` (MIT)
- `ISSUE_TEMPLATE/bug_report.md`
- `PULL_REQUEST_TEMPLATE.md`

### 9. 🏷️ GitHub Releases
> Tag releases on ROVA and countdown repos (e.g., `v1.0.0`) to look production-ready

### 10. 🎨 Consistent Repo Descriptions
> All repos should have a one-line description. Currently some are blank.

---

## 📊 Progress Tracker

| Task | Priority | Status |
|---|---|---|
| Fix snake animation (GitHub Actions) | 🔴 High | ✅ Done (pending push/run) |
| Pin top 6 repos | 🔴 High | ⏳ Pending |
| Fill GitHub profile sidebar | 🔴 High | ⏳ Pending |
| Add topics to all repos | 🔴 High | ⏳ Pending |
| ROVA README | 🟡 Medium | ⏳ Pending |
| board-exam-countdown README | 🟡 Medium | ⏳ Pending |
| Social preview images | 🟡 Medium | ⏳ Pending |
| Portfolio website | 🟡 Medium | ⏳ Pending |
| `.github/` templates | 🟢 Low | ⏳ Pending |
| GitHub Releases | 🟢 Low | ⏳ Pending |
| Consistent repo descriptions | 🟢 Low | ⏳ Pending |

---

> 💡 **Next Session Tip:** Start with the snake animation fix (15 min) + pin repos + fill sidebar (10 min). Then dive into individual repo READMEs starting with ROVA.
