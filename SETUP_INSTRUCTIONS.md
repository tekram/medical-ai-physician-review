# Setup Instructions

## ✅ Step 1: GitHub Pages (Enable Now)

1. Go to: https://github.com/tekram/medical-ai-physician-review/settings/pages
2. Under "Source", select: **Deploy from a branch**
3. Branch: **master** / **(root)**
4. Click **Save**
5. Wait 1-2 minutes for deployment

Your page will be live at: **https://tekram.github.io/medical-ai-physician-review/**

---

## ✅ Step 2: Formspree Setup (Get Form ID)

1. Go to: https://formspree.io/register (free account)
2. Click "New Form"
3. Form name: "Medical AI Physician Review"
4. Click "Create Form"
5. **Copy the Form ID** (looks like: `mzzbdpqr`)

---

## ✅ Step 3: Update Form ID in Code

Edit `index.html` line 175:

```javascript
// BEFORE:
const response = await fetch('https://formspree.io/f/YOUR_FORM_ID', {

// AFTER (use your actual form ID):
const response = await fetch('https://formspree.io/f/mzzbdpqr', {
```

Then commit and push:

```bash
cd physician-review-site
git add index.html
git commit -m "Add Formspree form ID"
git push
```

---

## ✅ Step 4: Share with ER Physician

Send them the URL:
**https://tekram.github.io/medical-ai-physician-review/**

They:
1. Visit URL
2. Fill in their info
3. Review 11 cases (~20-30 min)
4. Click "Submit All Reviews"
5. **You get email with their reviews!**

---

## How Formspree Works

- **Free tier**: 50 submissions/month
- **Email notification**: You get email when submitted
- **View submissions**: Check Formspree dashboard
- **Data format**: JSON with all review data

---

## Backup Plan (If Formspree Issues)

The page also saves to browser localStorage. If submission fails, you can ask them to:
1. Open browser console (F12)
2. Type: `localStorage.getItem('physician_reviews')`
3. Copy and send you the JSON

---

## Testing

Before sending to ER doc, test it yourself:
1. Visit the page
2. Complete one case
3. Submit
4. Check your email (connected to Formspree)

