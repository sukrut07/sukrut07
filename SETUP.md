# 🚀 Sukrut's GitHub Profile Setup Guide (Redesigned Edition)

This guide walks you through the configuration, workflows, and media customization for your redesigned GitHub profile (`sukrut07/sukrut07`).

---

## 📁 1. Assets Directory & Media Configuration

The following media files are located in [`assets/`](file:///Users/sukrutdusane/Documents/Projects%20/Sy/readme/assets):

| Asset | Size | Description |
|---|---|---|
| `assets/header.gif` | ~22 KB | "The Unknown" retro Starry Night pixel window animation (ultra-lightweight, looping). |
| `assets/footer.gif` | ~625 KB | The Joker pixel-art car ride animation (looping, under 1 MB). |
| `assets/connect.png` | ~40 KB | Michelangelo "Creation of Adam" retro dithered hands in a PROJECT.EXE window. |
| `assets/buymeacoffee.png` | ~4.7 KB | Official Buy Me a Coffee button linking to your profile. |

### 🎥 How to Use Native `<video>` Tags (Alternative to GIFs)
If you prefer native HTML5 MP4 videos over animated GIFs:
1. Open your repository `https://github.com/sukrut07/sukrut07` in your browser.
2. Click the edit pencil icon on `README.md` (or open any Issue comment box on GitHub).
3. Drag and drop your `.mp4` video file into the markdown editor.
4. GitHub will upload it and generate a URL like:
   ```
   https://github.com/user-attachments/assets/xxxx-xxxx-xxxx-xxxx
   ```
5. Copy that URL and uncomment the `<video>` tag in [README.md](file:///Users/sukrutdusane/Documents/Projects%20/Sy/readme/README.md) while commenting out the `<img>` tag:
   ```html
   <video src="https://github.com/user-attachments/assets/YOUR_ASSET_ID" autoplay loop muted playsinline width="100%" style="max-width: 720px; border-radius: 8px;"></video>
   ```

---

## ⚙️ 2. Workflows & GitHub Actions Setup

Your repository now includes 3 automated workflows in `.github/workflows/`:

| Workflow | Schedule | Purpose |
|---|---|---|
| [`galaga.yml`](file:///Users/sukrutdusane/Documents/Projects%20/Sy/readme/.github/workflows/galaga.yml) | Every 12 hrs (`0 */12 * * *`) | Generates animated Galaga fighter ship SVG shooting contribution blocks. Pushes to `output` branch. |
| [`profile-3d.yml`](file:///Users/sukrutdusane/Documents/Projects%20/Sy/readme/.github/workflows/profile-3d.yml) | Daily at 18:00 UTC | Generates 3D isometric contribution bar graphs (`profile-night-rainbow.svg`, `profile-green-animate.svg`). Pushes to `output` branch. |
| [`summary-cards.yml`](file:///Users/sukrutdusane/Documents/Projects%20/Sy/readme/.github/workflows/summary-cards.yml) | Daily at 00:00 UTC | Generates profile details, repos-per-language, most-commit-language, and productive time cards. Pushes to `output` branch. |

### Enabling Write Permissions
1. Go to repository **Settings** ➔ **Actions** ➔ **General**.
2. Under **Workflow permissions**, select **Read and write permissions**.
3. Check **Allow GitHub Actions to create and approve pull requests**.
4. Click **Save**.

### Triggering Workflows for the First Time
1. Go to the **Actions** tab on GitHub: `https://github.com/sukrut07/sukrut07/actions`.
2. For each workflow:
   - **Generate Galaga Game from GitHub Contribution Grid**
   - **GitHub Profile 3D Contrib**
   - **GitHub Profile Summary Cards**
3. Click the workflow name on the left ➔ Click **Run workflow** dropdown ➔ Select `Branch: main` ➔ Click **Run workflow**.

---

## 🏅 3. How to Add Credly Badges

Badges are organized into clean categories in `## 🏅 Verified Certifications & Digital Badges`.

To add a new badge:
1. Open your badge on your public Credly profile (`https://www.credly.com/users/sukrut-dusane`).
2. Right-click the badge image and copy the image address (`https://images.credly.com/images/<UUID>/image.png`).
3. Copy your verified badge link (`https://www.credly.com/badges/<UUID>`).
4. In `README.md`, add a `<td>` cell:

```html
<td align="center" width="25%">
  <a href="https://www.credly.com/badges/YOUR_BADGE_ID" target="_blank">
    <img src="https://images.credly.com/images/YOUR_IMAGE_ID/image.png" width="105" alt="Badge Title"/>
    <br/><b>Badge Title</b>
  </a>
</td>
```

---

## 📋 4. Review of Placeholders & Customizations

| Item | Location | Notes |
|---|---|---|
| **Featured Project Repos** | `## 📌 Featured Projects` | Pinned cards link to `agrin-regenerative-agricultural-intelligence1`, `mplads-ai-audit`, `ai-financial-journey`, and `federated-learning-system`. Update any repo names if you publish them under different slugs. |
| **Optional Tech Stack Badges** | `## 🛠️ Tech Stack` | Additional edge & federated AI badges (Flower, ONNX, MediaPipe) are included. You can delete any unused badges. |
| **LeetCode Status** | Entire README | Completely removed from social badges, about section, and stats per instructions. |
