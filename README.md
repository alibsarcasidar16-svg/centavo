# Centavo (₱) — Offline-First Envelope Budgeting

A lightweight, private, and offline-first personal finance web app designed specifically for the Philippine Peso (₱). Built with the **Sage & Paper** design system, pure integer centavo arithmetic, and zero server telemetry.

---

## Key Features

1. **Payday Quick Save & "Allocate Later" Pool**
   - Save your paycheck immediately in 2 seconds with zero math friction.
   - Allocates funds into a dedicated **Ready to Allocate** pool so you can budget into envelopes at your own pace without pressure.
   - Flexible custom split options (e.g. 30/30/30/10, 20/20/20/20/20, or custom percentages).

2. **Digital Envelope Budgeting**
   - Create custom envelopes (Food, Commute, Bills, Wants, Savings, etc.) with custom budget limits and icons.
   - 1-tap **Move Money** and **Cover Overspent** rebalancing to resolve budget deficits without guilt.

3. **Bills & Recurring Subscriptions**
   - Track monthly utilities and streaming subscriptions (Netflix, Spotify, PLDT, Meralco, Maynilad, etc.) with custom category icon badges.
   - 1-tap "Mark Paid" logging with automatic envelope and wallet deductions.

4. **GCash Reconcile & Clipboard Bridge**
   - Fast 2-second balance reconciliation.
   - Smart clipboard detection for GCash SMS/notification receipts.

5. **Financial Insights & Interactive Charts**
   - Spending by Category (Interactive Doughnut).
   - 30-Day Spending Trend (Interactive Area Chart with Category Filter).
   - Needs vs Wants vs Savings Compliance (50/30/20 Breakdown).
   - Daily Burn Rate vs Target Pace (Day-by-Day Bar Chart).
   - Budget Allocation vs Actual Spend (Planned vs Actual).

6. **Privacy & Aesthetics**
   - **Commuter Privacy Mode:** One-tap eye toggle to blur sensitive peso amounts in public or while commuting.
   - **3 Themes:** Sage Light, Obsidian Dark, and Baby Pink (Hello Kitty).
   - **Synthesized Haptic Audio:** Real-time Web Audio API sound feedback (clicks, chimes, coin drops).
   - **Animated Flame:** Live CSS flame effect celebrating your consecutive No-Spend streaks.

7. **Mathematical Integrity**
   - Pure integer centavo arithmetic (`₱1.00 = 100¢`). Zero floating-point rounding bugs.

---

## Deploying to Vercel

Centavo is configured for **Zero-Build Static Hosting** via `vercel.json`:

```json
{
  "version": 2,
  "buildCommand": null,
  "outputDirectory": ".",
  "cleanUrls": true,
  "rewrites": [
    { "source": "/(.*)", "destination": "/index.html" }
  ]
}
```

### Option A: Deploy via GitHub (Recommended)
1. Push this folder to a GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "feat: Centavo ready for deployment"
   git branch -M main
   git remote add origin https://github.com/<your-username>/centavo.git
   git push -u origin main
   ```
2. Go to [vercel.com](https://vercel.com) and log in.
3. Click **Add New Project** and select your `centavo` repository.
4. Leave **Framework Preset** as **Other** (Vercel automatically detects `vercel.json`).
5. Click **Deploy**. Your app will be live with an HTTPS `.vercel.app` domain in seconds!

### Option B: Deploy via Vercel CLI
If you have Node.js and Vercel CLI installed on your machine:
```bash
npm install -g vercel
vercel
```
Follow the interactive prompts to link and deploy.

### Option C: Deploy via Drag-and-Drop (Vercel Dashboard / Netlify / Cloudflare Pages)
- You can also drag the folder or upload `index.html`, `favicon.svg`, and `manifest.webmanifest` directly to any static web host.

---

## Credits
Built with care by **@kanda**.
