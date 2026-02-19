# Assessment Form: Setup Guide

A branded web form that collects assessment responses and emails them to you. Repeatable for every client. Takes 5 minutes to deploy.

## How it works

The form is a single HTML file. When a client submits it, the responses get emailed to david@thisisluminary.co via Formsubmit.co (free, no account needed). You also see a formatted table of their answers.

## Step 1: Deploy the form

**Option A: GitHub Pages (free, recommended)**
1. Create a new public repo: `buildfirst-assessment`
2. Upload `index.html` to the repo root
3. Go to **Settings > Pages > Source: Deploy from a branch > main**
4. Your form is now live at: `https://yourusername.github.io/buildfirst-assessment/`

**Option B: Netlify (free, drag and drop)**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the folder containing `index.html`
3. Done. You get a URL.

**Option C: Vercel (free)**
1. Import the repo at [vercel.com](https://vercel.com)
2. One click deploy

## Step 2: Verify your email (first time only)

The first time someone submits the form, Formsubmit.co will send a verification email to david@thisisluminary.co. Click the link to confirm. After that, all submissions go straight to your inbox.

## Step 3: Send to a client

Send them the URL with their details pre-filled:

```
https://your-url.com/?name=Bob+Hilb&company=Choice+Financial+Group&email=bob@email.com
```

The form pre-fills their name, company, and email. They just answer the questions.

## What you receive

An email with a clean table:
- Name, Company, Role, Email
- Energy ratings for 9 activities (1-5 scale)
- What they would hand off to a machine
- AI adoption level, tools used, sentiment
- Learning style, psychometric info
- The problem they want to solve (the important bit)

## Adding the database later

The form currently emails responses. To also store them in a spreadsheet:

1. Create a Google Sheet
2. Go to Extensions > Apps Script
3. Paste the webhook code (I can generate this when you are ready)
4. The form posts to both Formsubmit AND your Sheet

Or use Supabase for a proper database. But email works perfectly for the first 10-20 clients.
