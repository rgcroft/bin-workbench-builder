# Bin Workbench Builder

Interactive configurator for building storage-tote workbenches with wooden cubby frames. Supports 12-gallon and 27-gallon Greenmade/Costco totes with measured cubby dimensions.

## Features

- Configure rows/columns of bins in either size
- Choose frame material (2×4, plywood strips, furring strips)
- Orientation control (long side or short side on rails)
- Build-order cut list with pocket hole markings
- Isometric 3D SVG preview
- Sag warnings for furring strips on wide spans

## Deploy

Auto-deploys to Firebase Hosting on push to `main` via GitHub Actions.

### One-time setup

1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com)
2. In GitHub repo Settings → Secrets → Actions, add:
   - `FIREBASE_PROJECT_ID` — your Firebase project ID
   - `FIREBASE_SERVICE_ACCOUNT` — the JSON key for a Firebase service account (see below)
3. Push to `main` and the workflow handles the rest

### Getting the service account key

```bash
# Install Firebase CLI if needed
npm install -g firebase-tools

# Login
firebase login

# Create a service account key (replace PROJECT_ID)
# Go to: https://console.firebase.google.com/project/PROJECT_ID/settings/serviceaccounts/adminsdk
# Click "Generate new private key" → download the JSON
# Paste the entire JSON as the FIREBASE_SERVICE_ACCOUNT secret in GitHub
```

## Local dev

Just open `public/index.html` in a browser — it's a self-contained single-page app with no build step.
