# 🚀 Sukrut's GitHub Profile Setup Guide

This guide explains how to configure, test, and personalize your GitHub profile repository (`sukrut07/sukrut07`).

---

## 📁 1. Assets Directory Structure

Ensure the following files exist in the [`assets/`](file:///Users/sukrutdusane/Documents/Projects%20/Sy/readme/assets) directory before committing:

| File | Status | Description |
|---|---|---|
| `assets/header.png` | **Included (Placeholder)** | Transparent PNG banner image (Starry Night developer aesthetic, no background). You can replace this with any custom artwork. |
| `assets/footer.png` | **Included (Placeholder)** | Transparent PNG footer mascot (cute engineering rabbit with tools and laptop, no background). |
| `assets/buymeacoffee.png` | **Included (Official)** | Official Buy Me a Coffee button linking to `https://www.buymeacoffee.com/sukrut07`. |

> [!TIP]
> Both `assets/header.png` and `assets/footer.png` have been generated with transparency. If you replace them with your own artwork, ensure they are transparent PNG files for optimal display in both dark and light modes.

---

## ⚙️ 2. Enable GitHub Actions Write Permissions

The Pac-Man Contribution Grid workflow automatically commits animated SVGs (`pacman-contribution-graph.svg` and `pacman-contribution-graph-dark.svg`) to an orphan branch named `output`. To allow GitHub Actions to push to this branch:

1. Navigate to your profile repository on GitHub: `https://github.com/sukrut07/sukrut07`.
2. Click **Settings** (top tab).
3. In the left sidebar, click **Actions** ➔ **General**.
4. Scroll down to **Workflow permissions**.
5. Select **Read and write permissions**.
6. Check **Allow GitHub Actions to approve pull request requests** (optional, recommended).
7. Click **Save**.

---

## 🕹️ 3. Triggering the Pac-Man Workflow for the First Time

Once your files are pushed to GitHub:

1. Go to the **Actions** tab in your repository (`https://github.com/sukrut07/sukrut07/actions`).
2. Select **Generate Pacman Game from GitHub Contribution Grid** from the list of workflows on the left.
3. Click the **Run workflow** dropdown on the right.
4. Select `Branch: main` and click **Run workflow**.
5. Once the job completes (~1-2 minutes), an `output` branch will automatically be created containing your customized SVGs!
6. The README will immediately render the live animated Pac-Man grid. The workflow will automatically rerun every 12 hours.

---

## 🏅 4. How to Add Credly Badges

Credly badges are rendered as responsive, clickable image tiles inside an HTML `<table>` in the `## 🏅 Certifications & Badges` section of `README.md`.

To add a new badge:
1. Go to your badge on Credly (or your public profile at `https://www.credly.com/users/sukrut-dusane`).
2. Right-click the badge image and select **Copy Image Address** (format: `https://images.credly.com/images/<UUID>/image.png`).
3. Copy the URL of your verified badge page (format: `https://www.credly.com/badges/<UUID>`).
4. In `README.md`, locate the `## 🏅 Certifications & Badges` table.
5. Add a `<td>` cell:

```html
<td align="center" width="25%">
  <a href="https://www.credly.com/badges/YOUR_BADGE_ID" target="_blank">
    <img src="https://images.credly.com/images/YOUR_IMAGE_ID/image.png" width="115" alt="Badge Title"/>
    <br/>
    <b>Badge Title</b>
  </a>
</td>
```

> Each row holds up to 4 badges. For more than 4, start a new `<tr>` row.

---

## 📋 5. Assumptions & Placeholders to Review

| Item | Current Value in README | Action Needed |
|---|---|---|
| **Featured Project Repos** | `agrin-regenerative-agricultural-intelligence1`, `federated-learning-system`, `fraud-anomaly-detector`, `ai-financial-journey` | Verify repository names or update them to match your exact public repository slugs. |
| **Credly Badge Links** | AWS Certified Cloud Practitioner, AWS Solutions Architect Associate, AWS Developer Associate | Update badge IDs with your specific Credly verified credential URLs once ready. |
| **CodeChef Stats Card** | Skipped card in favor of LeetCode card (`jacoblin.cool`) | Public CodeChef card APIs are currently deprecated/unreliable, so profile badges are placed in the header, about, and footer sections. |
