# Deploying Resonae to Netlify

## Files You Need

You have 4 files that need to be uploaded to Netlify:

1. **index.html** - The main Resonae interface
2. **netlify.toml** - Configuration file
3. **package.json** - Dependencies
4. **netlify/functions/chat.js** - Backend function (in a folder)

## Step-by-Step Deployment Instructions

### Step 1: Download All Files

Download these files from Claude and keep them organized:
- Keep `chat.js` inside a folder structure: `netlify/functions/chat.js`

### Step 2: Create Netlify Account

1. Go to https://app.netlify.com/signup
2. Sign up with email or Google (whichever is easier)

### Step 3: Deploy Your Site

1. Once logged in, click "Add new site" → "Deploy manually"
2. You'll see a drag-and-drop area
3. **IMPORTANT:** You need to upload the entire folder structure, not individual files

**Option A - Create a ZIP file:**
- Put all files in a folder (maintaining the netlify/functions structure)
- Compress the folder as a ZIP
- Drag the ZIP file to Netlify

**Option B - Use GitHub (Recommended):**
- Upload all files to your GitHub resonae repository
- Maintain the folder structure (netlify/functions/chat.js)
- In Netlify, click "Import from Git" instead of manual deploy
- Connect to your GitHub account
- Select your resonae repository
- Netlify will automatically deploy

### Step 4: Add Your API Key (CRITICAL!)

After deployment:

1. In Netlify, go to your site settings
2. Click "Environment variables" in the left sidebar
3. Click "Add a variable"
4. Key: `ANTHROPIC_API_KEY`
5. Value: [paste your API key that you saved earlier - the one starting with sk-ant-api03-...]
6. Click "Create variable"
7. **Redeploy your site** (Deploys → Trigger deploy → Deploy site)

### Step 5: Test Your Site

1. Visit your Netlify URL (something like random-name.netlify.app)
2. Try sending a message to Resonae
3. She should respond!

## Troubleshooting

**If Resonae doesn't respond:**
- Check that you added the API key as an environment variable
- Make sure you redeployed after adding the key
- Check the browser console for errors (F12 → Console tab)

**If deployment fails:**
- Make sure the folder structure is correct: netlify/functions/chat.js
- Ensure all files are uploaded

## Need Help?

If you get stuck, take a screenshot of any error messages and I can help you troubleshoot!

---

Your Netlify URL will work on all devices - computer, phone, tablet.
Bookmark it and you'll have access to Resonae anywhere!
