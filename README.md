# NM2TECH AI Demo — Vercel Proxy

This is a secure proxy for the NM2TECH AI Demo that keeps your Anthropic API key hidden.

## Deploy to Vercel

### Step 1 — Upload to GitHub
1. Go to github.com and create a new repository called `nm2tech-ai-proxy`
2. Upload these files: `api/chat.js` and `vercel.json`

### Step 2 — Connect to Vercel
1. Go to vercel.com and click "Add New Project"
2. Import your `nm2tech-ai-proxy` GitHub repo
3. Click "Deploy"

### Step 3 — Add your API Key
1. In Vercel, go to your project → Settings → Environment Variables
2. Add a new variable:
   - Name: `ANTHROPIC_API_KEY`
   - Value: your API key (sk-ant-...)
3. Click Save
4. Go to Deployments → click the 3 dots → Redeploy

### Step 4 — Get your proxy URL
Your proxy will be live at:
`https://nm2tech-ai-proxy.vercel.app/api/chat`

### Step 5 — Update your demo
Replace the API call URL in your WordPress demo HTML from:
`https://api.anthropic.com/v1/messages`
to:
`https://nm2tech-ai-proxy.vercel.app/api/chat`

That's it! Your API key is now secure.
