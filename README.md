# Medical AI Safety Evaluation - Physician Review

Expert physician review interface for adversarial AI safety testing.

## Setup

### 1. Get Formspree Form ID

1. Go to https://formspree.io and sign up (free)
2. Create a new form
3. Copy the form ID (looks like: `xyzabc123`)
4. Replace `YOUR_FORM_ID` in `index.html` with your form ID

### 2. Deploy to GitHub Pages

```bash
git add .
git commit -m "Initial commit"
gh repo create physician-review --public --source=. --push
```

Then enable GitHub Pages:
- Go to repo Settings > Pages
- Source: Deploy from branch `main` → `/` (root)
- Save

### 3. Share URL

Your review page will be at: `https://[username].github.io/physician-review/`

## For Reviewers

Visit the hosted page, complete the review (~20-30 min), and click Submit. Reviews are automatically emailed to the research team.
